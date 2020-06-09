<properties
	pageTitle="Verify phase that takes longer"
	description="Verify phase that takes longer"
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
	articleId="94034c77-f7c6-4570-8db0-393c8d57eb15"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Verify phase that takes longer

Check our telemetry using the TaskId collected on the previous step

**Important:**  
	1. Make sure you are on the right MAB cluster
	2. Note only completed job will be seen.  If the job is still running make information will be still not available on this table 

To identify which phase of backup is taking time, run the below query:

~~~kusto

BCMBackupStats
   // |where PreciseTimeStamp > ago(7d) and VMName == "myVM"  //Use customer VMName here
    | where TaskId == <TaskId> // Replace <TaskId> with the guid collected on step 1
    | where TaskId == "205ae96d-7d89-480f-9654-78793af28a5d"
    | extend BackupDurationInHours = BackupTimeInMins/60
    | extend Queuetimeinmin = BackupQueueTimeInMilliSec/60000
    | extend TotalSnapshotTimeinmin =TotalSnapshotTimeInMilliSec/60000
    | extend  DiffCopyTimeInHours =  DiffCopyTimeInMilliSec/3600/1000
    | extend DurationInMin = DurationInMilliSec 
    | project  PreciseTimeStamp, StartTime ,  BackupDurationInHours,  TotalSnapshotTimeinmin, Queuetimeinmin,  DiffCopyTimeInHours, DeltaSizeInGB = (DeltaSizeInMB/1024), IsManagedVm, IsVMOffline, IsIR, TaskId

~~~

**Schema**

1. BackupDurationInHours - is the total backup time
2. TotalSnapshotTimeinmin - is the time dedicated to Snapshot phase
3. Queuetimeinmin - is the time dedicated for processing bewteen snapshot and transfer to the vault (copy) 
4. DiffCopyTimeInHours -  is the dedicated time to transfer to the vault (Copy) 

Compare the times of that job that run on the last 7 days for that VM  with previous ones to identify the phase that seems to have increased  

~~~kusto

BCMBackupStats
   |where PreciseTimeStamp > ago(7d) and VMName == "myVM"  //Use customer VMName here
    //| where TaskId == <TaskId> // Replace <TaskId> with the guid collected on step 1
    | where TaskId == "205ae96d-7d89-480f-9654-78793af28a5d"
    | extend BackupDurationInHours = BackupTimeInMins/60
    | extend Queuetimeinmin = BackupQueueTimeInMilliSec/60000
    | extend TotalSnapshotTimeinmin =TotalSnapshotTimeInMilliSec/60000
    | extend  DiffCopyTimeInHours =  DiffCopyTimeInMilliSec/3600/1000
    | extend DurationInMin = DurationInMilliSec 
    | project  PreciseTimeStamp, StartTime ,  BackupDurationInHours,  TotalSnapshotTimeinmin, Queuetimeinmin,  DiffCopyTimeInHours, DeltaSizeInGB = (DeltaSizeInMB/1024), IsManagedVm, IsVMOffline, IsIR, TaskId

~~~
