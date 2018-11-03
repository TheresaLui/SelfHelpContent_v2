<properties
	          pageTitle="usererrorunsupporteddisksize"
	          description="usererrorunsupporteddisksize"
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
## Backup operation was failing due to the disk size limit
<!--/issueDescription-->

## **Recommended steps**
Your backup operation could fail when backing up VM with disk size greater than 1023GB since your vault is not upgraded to Azure VM Backup stack V2. Upgrading to Azure VM Backup stack V2 will provide support up to 4TB. Review these [benefits](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2), [considerations](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2#considerations-before-upgrade), and then proceed to upgrade by following these [instructions](https://docs.microsoft.com/azure/backup/backup-upgrade-to-vm-backup-stack-v2#upgrade).
