<properties
	pageTitle="CopyingVHDsFromBackUpVaultTakingLongTime"
	description="CopyingVHDsFromBackUpVaultTakingLongTime"
	infoBubbleText="Backup failed because of system file errors.This could be due to one or more actions pending on this server"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-copyingvhdsfrombackupvaulttakinglongtime"
	diagnosticScenario="azurebackup-crc-copyingvhdsfrombackupvaulttakinglongtime"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CopyingVHDsFromBackUpVaultTakingLongTime

<!--issueDescription-->
We have identified that your backup operation is taking longer than expected, due to transient storage errors or insufficient storage account IOPS for the backup service to transfer data to the vault within the timeout period.
<!--/issueDescription-->

## **Recommended Steps**

* Review your Virtual Machine backup configuration
* Ensure you are using the [Best practices](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#best-practices) for Azure Backups
* Retry the operation

## **Recommended Documents**

* [Backup performance](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#backup-performance)
