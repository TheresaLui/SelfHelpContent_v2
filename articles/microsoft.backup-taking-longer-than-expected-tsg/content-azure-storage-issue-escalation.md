<properties
	pageTitle="Azure storage issue escalation"
	description="Azure storage issue escalation"
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
	articleId="85f25cea-a79f-4f68-a6e8-bfa8815c46f0"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Azure storage issue escalation

Please enage your TA and confirm on the insight page you dont see any livesite issue for Azure or might need the EEE/PG to debug this.

Also verify other corner scenarios:

1. **Disk Move**: For managed disks, Storage can change source disk's underlying resource to load balancing. When this happens, backup goes to CC (checksum compare) mode. CC mode is inherently slower then instant Restore mode (the default mode), requiring more time to complete. This requires no action from us, let the backup complete. And the next backup will probably go to instant Restore mode.

Run below query to check if disk move has happened

~~~kusto

TraceLogMessage 
| where TaskId == <"TaskID"> 
| where Message contains "Previous snapshot blob and current blob don\'t belong to the same parent blob | Params:" 
| project PreciseTimeStamp, Message | order by PreciseTimeStamp desc nulls last

~~~

Sample output:

Previous snapshot blob and current blob don't belong to the same parent blob | Params: {PreviousSnashotBlobAbsoluteUri = https://md-fkfsmc1c3l4r.blob.core.windows.net/ bjjwrhkfhhgb/abcd}{CurrentSnapshotBlobAbsoluteUri = https://md-fkfsmc1c3l4r.blob.core.windows.net/ d50c1042bkm3/abcd}

2. Check if any DiffApiFatalError occured

~~~kusto

    let _Time = datetime"<Time>";
    let _VMName = "<VMName>";
    BCMBackupStats
    | where PreciseTimeStamp > _Time 
    | where  VMName == _VMName
    | where TelemetryLogMessage contains "DiffApiFatalError"
    | project PreciseTimeStamp, TaskId, ErrorCode, TelemetryLogMessage, TelemetryRetryInfo

~~~

If we see in any results that means some DiffApiFatalError has occurred.
TelemetryRetryInfo will contain information if retry(Fallback to CC Mode) was attempted

e.g. TelemetryRetryInfo: "RetryFlow disabled as 16hr windows ends". Here no retry was attempted whereas in case
TelemetryRetyrInfo: "RetryTrigerred: VMAZBRPR3CX02_OsDisk_1_3d74e45fb4284d9c89787f851658bde7,errorCode: DiffApiFatalError", means retry was attempted

