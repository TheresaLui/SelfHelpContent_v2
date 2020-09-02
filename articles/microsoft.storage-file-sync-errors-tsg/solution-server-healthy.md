<properties
	pageTitle="How to check for sync errors"
	description="How to check for sync errors"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="02c6ea11-2126-4697-b3bd-43f4adda56ba"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check for sync errors
<!--issueDescription-->
1. Use ASC to view sync health. The sync health displayed in ASC is based on Event ID 9102 (HResult).
2. ASC > Resource Explorer > Storage Sync Service > Summary 
3. Select your sync group and display per-item errors
4. Obtain the HRESULT (example: -2147023673) and find it in [common sync errors article](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#common-sync-errors)

### Jarvis

1. If ASC is not available or the data is not up to date, use Jarvis to view the sync telemetry events. [Link to Jarvis](https://jarvis-west.dc.ad.msft.net/F40CF005)
    1. Event ID 9102 - Replica Sync session completed. Use this event to determine if a sync session completed successfully, how many files were transferred, per-item errors etc. 
    2. Event ID 9302 - Replica Sync Progress. Event ID 9302, 7005 and 7006 are progress events for a sync session. If a previous sync session failed, use the progress events to determine if sync is now working properly.
    3. Event ID 9121 – Per-Item Summary Event
	4. Obtain the HRESULT (example: -2147023673) and find it in [common sync errors article](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#common-sync-errors)


### Known issues:

1. Sync fail with ERROR_CANCELLED: 
    1. This is usually a transient issue; sync sessions can be cancelled for various reasons such as VSS snapshots or the server being restarted. If these errors persist for longer than a couple hours though, you should follow the steps below to troubleshoot.
2. Check to see if sync is still failing with E_CANCELLED (see Troubleshooting Sync Issues, Scenario 2 for how to use Jarvis to view the current sync health).
3. If sync still has not completely successfully, check to see if the previous sync session's SyncScenario was SnapshotSync. If so, the VSS snapshot is what caused sync to fail. Sync will retry; this is a transient issue that can be ignored.
4. We want to know if sync has made progress since the last session that was cancelled – it may be that the cancelled session was an ‘upload’ session but the next session which was started is a large ‘download’ session that is still in progress.
5. To know if the next session is making progress, [query event Id 9302](https://jarvis-west.dc.ad.msft.net/4925DCCC) from the last time event 9102 ended until the current time. If you see the AppliedFileCount and the AppliedSizeBytes numbers going up steadily, which means progress is being made, then sync should succeed soon and this error can be ignored. If these numbers are not increasing, that suggests that the next session is running but nothing is succeeding.
6. If nothing is succeeding, we should check whether there are many per-item errors causing this session to fail. See the section on troubleshooting per-item errors.
<!--/issueDescription-->