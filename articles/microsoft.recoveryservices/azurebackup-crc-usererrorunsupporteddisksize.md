<properties
	          pageTitle="usererrorunsupporteddisksize"
	          description="usererrorunsupporteddisksize"
		  infoBubbleText="Backup operation was failing due to the disk size limit"
	          service="microsoft.recoveryservices"
	          resource="backup"
	          authors="srinathv"
	          articleId="azurebackup-crc-usererrorunsupporteddisksize"
	          diagnosticScenario="azurebackup-crc-usererrorunsupporteddisksize"
	          selfHelpType="diagnostics"
	          supportTopicIds="32553276"
	          productPesIds="15207"
	          cloudEnvironments="public"
/>


# UserErrorUnsupportedDiskSize

<!--issueDescription-->
The backup operation failed because the disk exceeds the maximum allowed size by the VM Backup Stack v1. For disks bigger than 1023GB you need to upgrade to VM Backup stack V2. To avoid failures in the future, upgrade to Azure VM Backup stack V2.
<!--/issueDescription-->

## **Recommended steps**

* Review the [benefits](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2), including the ability to backup disks up to 4TB. 
* Make sure you read the [considerations](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2#considerations-before-upgrade) section.
* Complete the upgrade following these [instructions](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2#upgrade).
