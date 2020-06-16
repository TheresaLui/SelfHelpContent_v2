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

<!--/issueDescription-->

