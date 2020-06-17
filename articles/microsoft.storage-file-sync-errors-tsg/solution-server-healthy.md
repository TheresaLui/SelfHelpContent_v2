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
**ASC**
<br>
1. Use ASC to view sync health. The sync health displayed in ASC is based on Event ID 9102 (HResult).<br>
2. ASC > Resource Explorer > Storage Sync Service > Summary<br>
3. Select your sync group and display per-item errors<br>
4. Obtain the HRESULT (example: -2147023673) and find it in [common sync errors article](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#common-sync-errors)<br>
<br>
**Jarvis**<br>
<br>
1. If ASC is not available or the data is not up to date, use Jarvis to view the sync telemetry events. <br>
2. Event ID 9102 - Replica Sync session completed. Use this event to determine if a sync session completed successfully, how many files were transferred, per-item errors etc.<br>
3. Event ID 9302 - Replica Sync Progress. Event ID 9302, 7005 and 7006 are progress events for a sync session. If a previous sync session failed, use the progress events to determine if sync is now working properly.<br>
<br>
**Event ID 9121 – Per-Item Summary Event**
<br>
Obtain the HRESULT (example: -2147023673) and find it in [common sync errors article](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#common-sync-errors)
<!--/issueDescription-->