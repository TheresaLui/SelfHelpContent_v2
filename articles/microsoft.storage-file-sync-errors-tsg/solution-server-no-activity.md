<properties
	pageTitle="How to check if server endpoint health changed"
	description="How to check if server endpoint health changed"
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
	articleId="05e81f1b-a7d4-4653-b3f9-cd6667f666e9"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if server endpoint health changed

<!--issueDescription-->

**Problem**<br>
<br>
When I view the health of a server endpoint, the health status is "No Activity." When I view the status of the server under Registered Servers, the server has a status of Online.<br>

**Cause**<br>
<br>
A server endpoint health status of "No Activity" means the server endpoint has not logged sync activity in the past two hours.<br>
<br>
**Solution**<br>
<br>

1. A server endpoint may not log sync activity for the following reasons: The server has reached the maximum number of concurrent sync sessions. Azure File Sync currently supports 2 active sync sessions per processor or a maximum of 8 active sync sessions per server. The server has an active VSS sync session (SnapshotSync). When a VSS sync session is active for a server endpoint, other server endpoints on the server cannot start a start sync session until the VSS sync session completes.<br>

2. To check current sync activity on a portal: Within your sync group, go to the server endpoint in question and look at the Sync Activity section to see the count of files uploaded or downloaded in the current sync session. Note that this status will be delayed by about 5 minutes, and if your sync session is small enough to be completed within this period, it may not be reported in the portal.<br>

3. To monitor progress on the server: look at the most recent 9302 event in the telemetry log on the server in the Event Viewer, go to Applications and Services, Logs, Microsoft, FileSync, Agent, Telemetry. This event indicates the state of the current sync session. TotalItemCount denotes how many files are to be synced, AppliedItemCount the number of files that have been synced so far, and PerItemErrorCount the number of files that are failing to sync. <br>
4. More info [How do I monitor the progress of a current sync session?](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#how-do-i-monitor-the-progress-of-a-current-sync-session)

<br>

**Additional steps** <br>
<br>
**Jarvis File Sync Dashboards**

Please use the below dashboards to perform in-depth troubleshooting with any Azure File Sync scenario.


[Tiering and Recall](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FTiering%252520and%252520Recall&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738431233&sdata=E3tWbSS7XpFY42%2F%2FigkGVz0YYa%2B6LP%2FVsETkzuN4VDA%3D&reserved=0) : Used for Sync Tiering & Recall scenarios when Cloud Tiering is On.<br>           
[Sync Progress & Performance](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FSync%252520Progress%252520%252526%252520Performance&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738441190&sdata=7RlKn%2FH5K9wmvOCVPFyvjATEjFb58KpXCi8JRA0gFoY%3D&reserved=0): Used for tracking Sync Progress - both Upload & Download scenarios from SEP as well as Cloud-side Enumeration.<br>           
[SEP Health](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FSEP%252520Health&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738441190&sdata=8WJdLcSrEfIEZysiKDGfR5OyI3WFbRa6QZ7QFYb6zYo%3D&reserved=0): Used for viewing Agent & Filter details on SEP.<br> <br> 
[AFS Management](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fjarvis-west.dc.ad.msft.net%2Fdashboard%2FXEEE-Dashboards%2FFileSync%2FAFS%252520Management&data=02%7C01%7Cdroltean%40microsoft.com%7Cb10a9d3d669a4499e1b108d85be2bee8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637360376738441190&sdata=rXoJTp53%2FkfZLcUhiaImlyAs6r%2FGvnXTSNuHCOSZcco%3D&reserved=0): Used for viewing AFS Management operations.<br> 

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
- [Storage Sync Cloud Tiering](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-cloud-tiering)<br>
