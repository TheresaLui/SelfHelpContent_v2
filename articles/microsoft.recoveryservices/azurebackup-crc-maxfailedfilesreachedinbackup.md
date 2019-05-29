<properties
	pageTitle="MaxFailedFilesReachedInBackup"
	description="MaxFailedFilesReachedInBackup"
	infoBubbleText="The current backup operation failed because the number of data transfer failures was more than failure count"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-maxfailedfilesreachedinbackup"
	diagnosticScenario="azurebackup-crc-maxfailedfilesreachedinbackup"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error MaxFailedFilesReachedInBackup

<!--issueDescription-->
We have identified that your backup operation failed because the number of failed data transfers has reached the maximum number allowed.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue:

* Ensure that your volume has sufficient scratch space and the volume is not full
* Check that your backup agent is the [latest version available](https://azure.microsoft.com/resources/videos/download-install-and-register-the-azure-backup-agent/)
* If necessary, create additional space on the volume
* Retry the operation
