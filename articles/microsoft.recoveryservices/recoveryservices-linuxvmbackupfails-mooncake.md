<properties
	pageTitle="Backup of Linux Azure virtual machine fails with 'Could not communicate with the VM agent for snapshot status'"
	description="Linux VM Snapshot issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="2feefab9-c5ec-444c-a189-ae575462729f"
	ownershipId="Compute_SiteRecovery"
/>

# Backup of Linux Azure virtual machine fails with 'Could not communicate with the VM agent for snapshot status'

## **Recommended steps**
To resolve common isuess, try one or more of the following steps.

1. Check Linux VM agent is [up-to-date](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#cause-2-the-microsoft-azure-vm-agent-installed-in-the-vm-is-out-of-date-for-linux-vms)
2. Check VM has access to internet for taking snapshot. Learn how to [enable internet access](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#cause-1-the-vm-does-not-have-internet-access) if VM is behind NSG or Firewall. 
3. Check VMSnapshotLinux (extension used by Backup) is [up-to-date](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#cause-3-the-backup-extension-fails-to-update-or-load)
4. Check that snapshot status is [retrievable.](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#cause-4-the-snapshots-status-cannot-be-retrieved-or-the-snapshots-cannot-be-taken)


## **Recommended documents**
[Azure virtual machine backup troubleshooting guide](https://docs.azure.cn/backup/backup-azure-vms-troubleshoot)<br>
