<properties
	pageTitle="usererrorstandardssdnotsupported"
	description="usererrorstandardssdnotsupported"
	infoBubbleText="Currently Azure Backup does not support Standard SSD disks. See details on the right."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
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
Azure Backup currently does not support Standard SSD disks.
<!--/issueDescription-->

## **Recommended Steps**
Currently Azure Backup supports Standard SSD disks only for vaults that are upgraded to Azure VM Backup stack V2. 
* Review the [benefits](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2), including the ability to backup disks up to 4TB. 
* Make sure you read the [considerations](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2#considerations-before-upgrade) section.
* Complete the upgrade following these [instructions](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2#upgrade).
