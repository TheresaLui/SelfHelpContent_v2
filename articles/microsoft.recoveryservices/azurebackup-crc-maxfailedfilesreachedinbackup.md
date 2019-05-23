<properties
	pageTitle="MaxFailedFilesReachedInBackup"
	description="MaxFailedFilesReachedInBackup"
	infoBubbleText="The current backup operation failed because the number of data transfer failures was more than failure count"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author:"srinathv"
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
We have identified that your backup operation failed, because the number of data transfer failures was more than failure count.
<!--/issueDescription-->

## **Recommended Steps**
To resolve MaxFailedFilesReachedInBackup check if the volume where scratch space is configured is not full and retry the operation and ensure backup agent installed is latest.
