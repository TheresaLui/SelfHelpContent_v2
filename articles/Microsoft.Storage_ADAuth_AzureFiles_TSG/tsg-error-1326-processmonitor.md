<properties
    pageTitle="Computer Identity is used to access Azure Files"
    description="Computer Identity is used to access Azure Files"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="cbaf527c-36c4-48ca-9f4f-af3578176758"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Use Process Monitor to determine the user identity of the process getting access denied

## Customer detection

1. Download [Process Monitor](https://docs.microsoft.com/sysinternals/downloads/procmon) and install it on customer's machine. 
2. Collect a Process Monitor trace and right click on the event where Access was denied.
example here. 
3. Click on the **Process** tab. 
![](Screenshots\Error_Logon_Failure1.png)
4. **User** section will show the SID of the User. 
![](Screenshots\Error_Logon_Failure2.png)
5. If it's **NT AUTHORITY\SYSTEM**, you can assume the process is using the SID of the computer on the network.
6. If it's another SID, use PowerShell to covert SID to Active Directory Object. Example of computer object. 

        PS F:\gitroot> $SID = 'S-1-5-21-2127521184-1604012920-1887927527-12933720'
        PS F:\gitroot> Get-ADObject -Filter "objectSid -eq '$sid'" | Select-Object name, objectClass
        name          objectClass
        ----          -----------
        machine23     computer
        
## Xstore Detection

Because customer follow-up on process monitor information can take time, you can also check XDS logs to see if computer account is detected.
1. Find a UTC time range of when the issue was reported.
2. Do an XDS search on XSMBServer role for TreeConnect failures with error c000006d
3. Find the perf log

    perf: XSmbServer.exe: PerfCounters: Account=testingkerbsess3nad01D5B79DAD39006B SmbCommand=TreeConnect Operation=TreeConnect Details= on Container=share01 with Status=Failure StatusCode=c000006d InternalStatus=ClientOtherError Client=40.86.165.x:50786 Session=1e8402200001a5 SmbMsgId=9 RequestSize=190 ResponseSize=125 TimeInMs=73.887 ProcessingTimeInMs=73.828 RequestUrl=testingkerbsess3nad.file.preprod.core.windows.net\share01\ FileId=0 HandleId=0 TotalTableServerTimeInMs=0.644 TotalTableServerRoundTripCount=1 LastTableServerInstanceName=sat09prdste01d:xtableserver_in_19 LastTableServerErrorCode=80004005 TotalXStreamOpenTimeInMs=0.000 TotalXStreamOpenRoundTripCount=0 TotalXStreamIOTimeInMs=0.000 TotalXStreamIORoundTripCount=0 TotalXFERoundTripTimeInMs=0.000 TotalXFERoundTripCount=0 TotalThrottleTimeInMs=0 TotalThrottleCount=0 TotalRetryBackoffTimeInMs=0.000 TotalRetryBackoffCount=0 FileThrottlingCount=0 
    01/06/2020 15:00:58.018980 - pid: 106336 tid: 53568 @ ShimUpdateQuantilesAndPerfCounters (analytics.cpp:3323) 
    on ms-sat09prdste01a:xsmbserver_in_14  / cosmosPerfLog_XSmbServer.exe_000282.bin  /  29E462F5-501D-000E-00A2-C42AB0000000

4. Click the activity ID in the perf log. 

    You will see a logging statement, something like info: 
    
    **XSmbServer.exe: FilterWellKnownSids:: Found matching non-alerting Sid with patternIndex: 0** 
    
    If this is present, a computer SID has been detected.