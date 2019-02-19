<properties
	pageTitle="usererrorolrnotsupported"
	description="usererrorolrnotsupported"
	infoBubbleText="The selected restore operation type is not supported."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	authorAlias="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorolrnotsupported"
	diagnosticScenario="azurebackup-crc-usererrorolrnotsupported"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# UserErrorOlrNotSupported

<!--issueDescription-->
## **Restore operation failed because you are performing a 'Replace existing' operation for an unsupported scenario. **
<!--/issueDescription-->

## **Recommended Steps**
We have identified that your restore failed because you are performing [**Replace existing**](https://docs.microsoft.com/en-us/azure/backup/backup-azure-arm-restore-vms#replace-existing-disks) operation for an [unsupported scenario](https://docs.microsoft.com/en-us/azure/backup/backup-azure-arm-restore-vms#restore-options)

To resolve this issue, use [**Create New**](https://docs.microsoft.com/en-us/azure/backup/backup-azure-arm-restore-vms#create-new-restore-disks) option instead of **Replace existing** option.

## **Recommended Document**
For more information on how to chose the correct restore operation see this [article](https://azure.microsoft.com/blog/an-easy-way-to-bring-back-your-azure-vm-with-in-place-restore/).
