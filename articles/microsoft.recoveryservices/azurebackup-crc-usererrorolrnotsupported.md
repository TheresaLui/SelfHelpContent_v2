<properties
	pageTitle="usererrorolrnotsupported"
	description="usererrorolrnotsupported"
	infoBubbleText="The selected restore operation type is not supported."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorolrnotsupported"
	diagnosticScenario="AzureBackup_ScenarioLevelInsight"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# UserErrorOlrNotSupported

<!--issueDescription-->
**Restore operation failed because you are performing a 'Replace existing' operation for an unsupported scenario.**
<!--/issueDescription-->

## **Recommended Steps**

We have identified that your restore failed because you are performing a [**Replace existing**](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#replace-existing-disks) operation for an [unsupported scenario](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-options).

To resolve this issue, use the [**Create New**](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#create-new-restore-disks) option instead of **Replace existing**.

## **Recommended Documents**

* [Choose the correct restore operation](https://azure.microsoft.com/blog/an-easy-way-to-bring-back-your-azure-vm-with-in-place-restore/)
