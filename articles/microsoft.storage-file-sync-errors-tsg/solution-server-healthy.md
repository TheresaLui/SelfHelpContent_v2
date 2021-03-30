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

2. **Additional steps:** <br>
**Jarvis File Sync Dashboards**

	Please use the below dashboards to perform in-depth troubleshooting with any Azure File Sync scenario.


	[Tiering and Recall](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FTiering%252520and%252520Recall&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738431233&sdata=E3tWbSS7XpFY42%2F%2FigkGVz0YYa%2B6LP%2FVsETkzuN4VDA%3D&reserved=0) : Used for Sync Tiering & Recall scenarios when Cloud Tiering is On.<br>           
	[Sync Progress & Performance](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FSync%252520Progress%252520%252526%252520Performance&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738441190&sdata=7RlKn%2FH5K9wmvOCVPFyvjATEjFb58KpXCi8JRA0gFoY%3D&reserved=0): Used for tracking Sync Progress - both Upload & Download scenarios from SEP as well as Cloud-side Enumeration.<br>           
	[SEP Health](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FSEP%252520Health&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738441190&sdata=8WJdLcSrEfIEZysiKDGfR5OyI3WFbRa6QZ7QFYb6zYo%3D&reserved=0): Used for viewing Agent & Filter details on SEP.<br> <br> 
	[AFS Management](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FAFS%252520Management&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738441190&sdata=rXoJTp53%2FkfZLcUhiaImlyAs6r%2FGvnXTSNuHCOSZcco%3D&reserved=0): Used for viewing AFS Management operations.<br> 


<br>

### Known issues:

1. Sync fail with ERROR_CANCELLED: 
     This is usually a transient issue; sync sessions can be cancelled for various reasons such as VSS snapshots or the server being restarted. If these errors persist for longer than a couple hours though, you should follow the steps below to troubleshoot.
2. Check to see if sync is still failing with E_CANCELLED (see Troubleshooting Sync Issues, Scenario 2 for how to use Jarvis to view the current sync health).
3. If sync still has not completely successfully, check to see if the previous sync session's SyncScenario was SnapshotSync. If so, the VSS snapshot is what caused sync to fail. Sync will retry; this is a transient issue that can be ignored.
4. We want to know if sync has made progress since the last session that was cancelled – it may be that the cancelled session was an ‘upload’ session but the next session which was started is a large ‘download’ session that is still in progress.
5. To know if the next session is making progress, [query event Id 9302](https://jarvis-west.dc.ad.msft.net/4925DCCC) from the last time event 9102 ended until the current time. If you see the AppliedFileCount and the AppliedSizeBytes numbers going up steadily, which means progress is being made, then sync should succeed soon and this error can be ignored. If these numbers are not increasing, that suggests that the next session is running but nothing is succeeding.
6. If nothing is succeeding, we should check whether there are many per-item errors causing this session to fail. See the section on troubleshooting per-item errors.<br>
<br>
#
# Escalation

<!--issueDescription-->
If your issue was not resolved, please use the below options to escalate your issue. <br> 
<br>
We suggest using the feedback link below to describe the circumstances of your case so they can be accounted for in future revisions of this TSG.<br>
<br>
If this TSG was not able to solve your issue and you are still experiencing issues, please leverage the following resources:<br>

1. Make an [AVA Channel](https://teams.microsoft.com/l/channel/19%3a359d3e19232242b48286d8076579389f%40thread.skype/File%2520Sync%2520Services%2520-%2520All%2520Topics?groupId=082ae864-dfc1-4ae5-b096-6e1e878b339e&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) post in the Storage SME File Sync Services channel<br>
2. Get advisement from your TA or peers<br>
3. [Create an ICM to Xstore EEE](http://aka.ms/cri-xeee)<br>
4. If you reached this page by mistake, please click the Start Over button to start the TSG from the beginning. Otherwise, you can close this window.<br>

<!--/issueDescription-->

## Recommended Documents

- [Planning for an Azure File Sync deployment](https://docs.microsoft.com/azure/storage/files/storage-sync-files-planning)<br>
- [Deploy Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal)<br>
- [Planning Data Migration with Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-files-migration-overview)<br>
- [Add/Remove server endpoint in Sync group](https://docs.microsoft.com/azure/storage/files/storage-sync-files-server-endpoint)<br>
- [Frequently asked questions (FAQ) about Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-files-faq#azure-file-sync)<br>
- [Monitor Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-monitoring)<br>
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal)<br>
- [Storage Sync Cloud Tiering](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-cloud-tiering)
<!--/issueDescription-->