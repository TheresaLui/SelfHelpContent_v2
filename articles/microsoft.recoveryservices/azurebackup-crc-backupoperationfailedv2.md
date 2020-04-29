<properties
	pageTitle="Backup failed with an internal error"
	description="Backup failed with an internal error"
	infoBubbleText="Backup failed with an internal error."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-backupoperationfailedv2"
	diagnosticScenario="azurebackup-crc-backupoperationfailedv2"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Backup failed with an internal error

<!--issueDescription-->
## **Backup failed with an internal error**
<!--/issueDescription-->

## **Recommended Steps**

Azure Backup service initiates the backup job by communicating with the VM backup extension to take a point-in-time snapshot. We have identified that your backup operation failed because the snapshot isn't triggered. To resolve this issue, follow [these](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#backupoperationfailed--backupoperationfailedv2---backup-fails-with-an-internal-error) steps.
