<properties
	pageTitle="Backup of Linux Azure virtual machine fails"
	description="Linux VM Snapshot issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32553276"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Backup of Linux Azure virtual machine fails

## **Recommended steps**
To resolve common isuess, try one or more of the following steps.

Ensure your [**Linux VM agent**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms) is up to date before troubleshooting further <br> 

Ensure there is [**connectivity**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-vm-has-no-internet-access) between VM and Azure Storage endpoints <br>  

Ensure the VM [**Linux OS version and Kernel version are compatible**](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#supported-operating-systems-for-backup) for using Azure Backup. If your OS/Kernel version is not in the distribution list then it not supported for Azure Backup [**connectivity**] <br>  

Backup can fail due to Snapshot extension issues, [**uninstall the extension to force reload**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load) and retry the operation <br>

## **Recommended documents**
If above steps does not resolve your issue, check [Azure virtual machine backup troubleshooting guide](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout) for the error message, causes and solutions<br>
