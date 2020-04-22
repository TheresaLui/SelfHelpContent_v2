<properties
	pageTitle="SalVhdBackupPrepareFailed"
	description="SalVhdBackupPrepareFailed"
	infoBubbleText="An unexpected error occurred during the operation."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc- salvhdbackuppreparefailed"
	diagnosticScenario="azurebackup-crc- salvhdbackuppreparefailed"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error SalVhdBackupPrepareFailed

<!--issueDescription-->
We have identified your backup operation failed  because of insufficient space on cache (scratch) location on selected VHD or volume.
<!--/issueDescription-->

## **Recommended Steps**

- To resolve this issue follow recommended guidelines list [here](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#whats-the-minimum-size-requirement-for-the-cache-folder) to ensure cache (scratch) folder has free space.
