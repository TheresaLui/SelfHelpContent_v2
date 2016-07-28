<properties
	pageTitle="Backup of Windows VM fails with 'Could not communicate with the VM agent for snapshot status'"
	description="Windows VM Snapshot issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Backup of Windows VM fails with 'Could not communicate with the VM agent for snapshot status'

## **Recommended steps**
To resolve common isuess, try one or more of the following steps.

1. Check VM has access to internet for taking snapshot. Learn how to [enable internet access](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-1-the-vm-does-not-have-internet-access) if VM is behind NSG or Firewall. 
2. Check VMSnapshot extension (extension used by Backup) is [up-to-date](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-3-the-backup-extension-fails-to-update-or-load)
3. Check that snapshot status is [retrievable.](https://azure.microsoft.com/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-4-the-snapshots-status-cannot-be-retrieved-or-the-snapshots-cannot-be-taken)


## **Recommended documents**
[Azure virtual machine backup troubleshooting guide](https://azure.microsoft.com/documentation/articles/backup-azure-vms-troubleshoot/)<br>
