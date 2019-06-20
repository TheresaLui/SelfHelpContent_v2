<properties
	pageTitle="ExtensionFailedSnapshotRateExceededError"
	description="ExtensionFailedSnapshotRateExceededError"
	infoBubbleText="Backup operation failed as the snapshot call coincided with another snapshot request from a different client"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	articleId="azurebackup-crc-extensionfailedsnapshotrateexceedederror"
	diagnosticScenario="azurebackup-crc-extensionfailedsnapshotrateexceedederror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# ExtensionFailedSnapshotRateExceededError

<!--issueDescription-->
We have identify that the backup snapshot operation is colliding with another product trying to take snapshot at the same time. Since the storage account has a limit of one snapshot, per disk per minute hence the backup failed.
<!--/issueDescription-->

## **Recommended Document**
To resolve this issue, ensure there is no conflict during snapshot operation, by following the [best practices](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#best-practices) and retry the backup operation.
