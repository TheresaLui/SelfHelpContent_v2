<properties
	pageTitle="Check what is causing the copy to take longer"
	description="Check what is causing the copy to take longer"
	service=""
	resource=""
	authors="TestAuthor"
	ms.author="TestAuthor"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="4ce8e391-fb32-4d0e-b098-260d22099ac6"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check what is causing the copy to take longer

Check our telemetry using the TaskId  collected on the previous step .

**Important:**  
	1. Make sure you are on the right MAB cluster
	2. Note running job can also be seeing in this query , not only completed ones .

1. Check high churn. Use the following Kusto query to find out churn on customer's VM

~~~kusto

let _TaskId = "<Taskid>"; //replace with TaskId 
let _Time = ago(10d); // time range the taskId is in (this from 10 days ago to today)
let _TraceLogs = TraceLogMessage
| where PreciseTimeStamp > _Time
| where TaskId == _TaskId
| where ServiceName == "dc"
| project PreciseTimeStamp, TaskId, RoleInstance, ResourceName, ResourceId, FileNameLineNumber, Message, Level;
let T1 = _TraceLogs
| where Message startswith "Writing data for diff range"
| extend Offset = extract("StartOffset = (.+?)}", 1, Message, typeof(long))
| extend RangeSizeTransferred = extract("rangeSize = (.+?)}", 1, Message, typeof(long))
| distinct ResourceName, Offset, RangeSizeTransferred
| summarize DataTransferredInGB = sum(RangeSizeTransferred) / 1024 / 1024 / 1024 by ResourceName;
let T2 = _TraceLogs
| where Message startswith "Updated copy status"
| extend PercentDone = extract("PercentCompleted = (.+?)}", 1, Message, typeof(long))
| summarize max(PercentDone) by ResourceName;
T1 | join (T2) on ResourceName
| project ResourceName, max_PercentDone, DataTransferredInGB

~~~

If DataTransferedinGB here is more tha(2-5 % of original disk size) 200gb+ , churn is high.  

2. Check if fragmentation. First, locate the vhd that is taking most of the time using the below Kusto query.

~~~kusto

TraceLogMessage 
| where TaskId == <TaskId >  
| where PreciseTimeStamp > datetime(<start time >)  // replace with start  of the job example datetime(2019-11-25 14:33:46.0)
| where Message contains ?Diff copy transfer for Vhd completed? | project Message, RoleInstance

~~~

The output will throw this message for each of the VM's disk.

Here is a sample log:

~~~log

StartStatusUpdate: Diff copy transfer for Vhd completed. | Params: {Operation state = Completed}{TotalBackupTime = 1.07:45:30.1466258}{TotalOperationTime = 1.07:45:32.3109242}{Vhd Id = VAZUSWTSTDB01-VAZUSWTSTDB01-2-201603180527190473}{Transferred blocks = 103}

~~~

1. Look at the backup time for all VHDs and make a note of role instance taking the highest backup time. There may be more than one disk that can be slow in backup.
2. Now, filter further on trace log message table by role instance of disks you see are taking longer time to backup
3. In some cases due to high fragmentation, pageDiffRanges return large number of ranges, resulting slow backup performance.
4. To verify the high fragmentation use below Kusto query once you indentify the disk and Roleinstance above
5. When you run below Kusto query for the first time, uncomment the second last line.
6. When you run the below Kusto query second time, uncomment the last line.

~~~kusto 

    let WindowStartOffset = 0; 
    let WindowEndOffset = 3375500697272320; 
    let _16KB = 16 * 1024; 
    TraceLogMessage 
    | where PreciseTimeStamp > datetime(<update date time>) and PreciseTimeStamp < datetime(<update date time>)  
    | where ServiceName == "dc" 
    | where TaskId == "<taskid>" 
    | where RoleInstance == "<suspected slow role instance name>" 
    | where Message startswith "Printing diff ranges : " 
    | project PreciseTimeStamp, TaskId, Message 
    | extend FirstOffsetStr = substring(Message, 0, 100) 
    | extend FirstStartOffset = tolong(extract(@'Printing diff ranges : \( (.+?),(.*)', 1, FirstOffsetStr)) 
    | project TaskId, PreciseTimeStamp, FirstStartOffset, Message  
    | extend FirstStartOffset = bin(FirstStartOffset, _16KB) 
    | where FirstStartOffset <= WindowEndOffset 
    | parse kind=regex Message with @"Printing diff ranges :" KeyValuePairs @"," 
    | project TaskId, PreciseTimeStamp, KeyValuePairs  
    | extend tmp = split(KeyValuePairs, ')') 
    | mvexpand tmp limit 100000000 
    | where tmp != "" 
    | parse kind=regex tmp with @"(.*?)" InputStartOffset:long @"," InputEndOffset:long @",(.*)" 
    | project-away KeyValuePairs , tmp  
    | extend InputStartOffset =  bin(InputStartOffset, _16KB) 
    | extend InputEndOffset = ceiling(toreal(InputEndOffset) / _16KB) * _16KB - 1 
    | extend Length  = InputEndOffset - InputStartOffset + 1 
    //| count // first query: uncomment this line and then run this query 
    //| summarize percentile(Length, 90) // second query: uncomment this line and then run this query

~~~

**Output**

After running first query, if the count is in lakhs this indicates high fragmentation.
After running second query, if the 90th percentile value of Length of the diffPageRange is around 16KB to 48KB. This indicates high fragmentation.
