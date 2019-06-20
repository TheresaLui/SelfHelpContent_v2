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
	cloudEnvironments="public"
/>

# Error CopyingVHDsFromBackUpVaultTakingLongTime

<!--issueDescription-->
We have identified that your backup operation is taking longer than expected.
<!--/issueDescription-->

## **Recommended Steps**
We have identified that the backup operation failed becuase due to transient storage errors or insufficient storage account IOPS for backup service to transfer data to the vault within the timeout period.

## **Recommended Document**
To resolve this issue, configure VM backup using these best practices and retry the backup operation. For more information, refer [Backup performance](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#backup-performance) and [Best practices](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#best-practices).
