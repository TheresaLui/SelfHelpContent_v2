<properties
	pageTitle="MaxFailedFilesReachedInBackup"
	description="MaxFailedFilesReachedInBackup"
	infoBubbleText="The current backup operation failed because the number of data transfer failures was more than failure count"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-maxfailedfilesreachedinbackup"
	diagnosticScenario="azurebackup-crc-maxfailedfilesreachedinbackup"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error MaxFailedFilesReachedInBackup

<!--issueDescription-->
We have identified that your backup operation failed, because the number of data transfer failures was more than the permissible failure count (default is 1000 failures).
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform the below troubleshooting steps and retry the operation:

* Ensure backup agent installed is latest
* Check if the volume where scratch space is configured exists (not deleted)
* Ensure the scratch folder is not full
* Ensure MARS agent is excluded from the antivirus installed on the machine
* Check if disk defragmentation is enabled on protected datasource volume. Test by disabling Disk defragmentation for the protected datasource and uncheck.
* Automatically Optimize new drives option and ensure the metadata VHD mounted is not getting defragmented
