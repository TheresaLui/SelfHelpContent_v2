<properties
	pageTitle="usererrorstandardssdnotsupported"
	description="usererrorstandardssdnotsupported"
	infoBubbleText="Currently Azure Backup does not support Standard SSD disks. See details on the right."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorstandardssdnotsupported"
	diagnosticScenario="azurebackup-crc-usererrorstandardssdnotsupported"
	selfHelpType="diagnostics"
	supportTopicIds="32553276,32553277,32553285"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# UserErrorStandardSSDNotSupported

<!--issueDescription-->
We found that you are using Standrd SSD disk for this **<!--$DatasouceName-->DatasouceName<!--/$DatasouceName-->** VM. However, Azure Backup currently does not support Standard SSD disks for vaults that are not upgraded to Azure VM Backup stack v2. 
<!--/issueDescription-->

## **Recommended Steps**

To verify and upgrade this **<!--$VaultName-->VaultName<!--/$VaultName-->** vault to Azure VM Backup Stack V2, see this [article](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2). <br>
Make sure you read the [considerations](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2#considerations-before-upgrade) section.

## **Recommended Documents**
Review the [benefits](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2), including the ability to backup disks up to 4TB. 
