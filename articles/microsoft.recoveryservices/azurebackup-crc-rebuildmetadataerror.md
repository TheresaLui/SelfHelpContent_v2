<properties
	pageTitle="RebuildMetadataError"
	description="RebuildMetadataError"
	infoBubbleText="Microsoft Azure Recovery Services Agent was unable to initialize a backup storage location with Microsoft Azure BackupError."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-rebuildmetadataerror"
	diagnosticScenario="azurebackup-crc-rebuildmetadataerror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error RebuildMetadataError

<!--issueDescription-->
We have identified that your backup operation failed because the Microsoft Azure Recovery Services Agent was unable to initialize a backup storage location with Microsoft Azure Backup.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, perform the below steps:

- Retry the operation. If the issue is transient, retry will resolve the issue. 
- If issue persists, [review the prerequites and troubleshooting steps for Cache folder](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#troubleshoot-cache-problems)
