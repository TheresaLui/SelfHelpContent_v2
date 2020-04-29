<properties
	pageTitle="AnotherWSBJobRunning"
	description="AnotherWSBJobRunning"
	infoBubbleText="The operation failed because another job is running on Windows Server Backup."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-anotherwsbjobrunning"
	diagnosticScenario="azurebackup-crc-anotherwsbjobrunning"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error AnotherWSBJobRunning

<!--issueDescription-->
## We have identified that Windows Server Backup (WSB) might be running a backup job or it is in frozen state.
<!--/issueDescription-->

## **Recommended Steps**
The Windows Server Backup (WSB) is internally used by MARS agent to perform System State backups, so WSB should be in running state.<br/>
To resolve AnotherWSBJobRunning issue perform the below:

* Stop any frozen or long running backup on WSB which is not triggered
* Reboot the server and retry the backup operation
