<properties
	pageTitle="azure iaas vm backup/register or back up a windows virtual machine"
	description="azure iaas vm backup/register or back up a windows virtual machine"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="kasparks"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553277"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="MoonCake"
/>

# azure iaas vm backup/register or back up a windows virtual machine

## **Recommended steps**
To resolve the most common issues, try one or more of the following steps
* Make sure VM has internet access for taking snapshot
[Enable internet access for Virtual machines under NSG or Firewall.](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#cause-1-the-vm-does-not-have-internet-access)

* Check VMSnapshot Extension is up to date
[Steps to ensure that the extension is up to date](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#cause-3-the-backup-extension-fails-to-update-or-load)

* Check Status of the snapshot taken can be retrieved
[Steps to ensure snapshot status is retrievable](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#cause-4-the-snapshots-status-cannot-be-retrieved-or-the-snapshots-cannot-be-taken)

* My VM Backup is slow
[Factors contributing to backup Time](https://docs.azure.cn/backup/backup-azure-vms-introduction#total-vm-backup-time)

* Check if you are following Best Practices to optimize backup performance
[Best practices for optimal backup performance](https://docs.azure.cn/backup/backup-azure-vms-introduction#best-practices)

## **Recommended documents**
[Azure virtual machine backup troubleshooting guide'](https://docs.azure.cn/backup/backup-azure-vms-troubleshoot)
