<properties
	pageTitle="WSBDiskSpaceOrSFCIssue"
	description="WSBDiskSpaceOrSFCIssue"
	infoBubbleText="Windows Server Backup failed to backup System State"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-azurebackup-crc-wsbdiskspaceorsfcissue"
	diagnosticScenario="azurebackup-crc-azurebackup-crc-wsbdiskspaceorsfcissue"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# WSBDiskSpaceOrSFCIssue 

<!--issueDescription-->
Your backup operation failed because there might not be enough space on the Scratch folder volumes.
<!--/issueDescription-->

## **Recommended Steps**

- Ensure there is at least 30 GB free of space on system volume (usually C:) for System State Backup, [Learn more](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#whats-the-minimum-size-requirement-for-the-cache-folder) <br>(or)
- Move the scratch location to a drive has the good amount of free space as steps mentioned in this [article](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#how-do-i-change-the-cache-location-for-the-mars-agent)
