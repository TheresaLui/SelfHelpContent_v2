<properties
	pageTitle="usererrorstandardssdnotsupported"
	description="usererrorstandardssdnotsupported"
	infoBubbleText="Currently Azure Backup does not support Standard SSD disks. See details on the right."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	authorAlias="srinathv"
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
Azure Backup currently supports Standard SSD disks only for vaults that are upgraded to Azure VM Backup stack v2.
<!--/issueDescription-->

## **Recommended Steps**

To solve this problem you will need to upgrade to the [Azure VM Backup Stack V2](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2). <br>
Make sure you read the [considerations](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2#considerations-before-upgrade) section.

## **Recommended Documents**
Review the [benefits](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2), including the ability to backup disks up to 4TB. 
