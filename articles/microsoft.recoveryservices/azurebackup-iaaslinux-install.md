<properties
	pageTitle="Azure iaas vm backup/register or back up a linux virtual machine"
	description="Azure iaas vm backup/register or back up a linux virtual machine"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="kasparks"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553276"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a77142cc-8a49-48ab-965c-4ad278e5cab0"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure iaas vm backup/register or back up a linux virtual machine
## **Recommended steps**
To resolve the most common issues, try one or more of the following steps
* Check VM agent installed is up to date. <br>
[Update Linux VM agent](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-2-the-microsoft-azure-vm-agent-installed-in-the-vm-is-out-of-date-for-linux-vms)

* Make sure VM has internet access for taking snapshot <br>
[Enable internet access for Virtual machines under NSG or Firewall](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-1-the-vm-does-not-have-internet-access)

* Check VMSnapshotLinux Extension is up to date <br>
[Steps to ensure that the extension is up to date](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout/#cause-3-the-backup-extension-fails-to-update-or-load)

* My VM Backup is slow <br>
[Factors contributing to backup Time](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-vms-introduction/#total-vm-backup-time)

* Check if you are following Best Practices to optimize backup performance <br>
[Best practices for optimal backup performance](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-vms-introduction/#best-practices)

## **Recommended documents**
[Azure virtual machine backup troubleshooting guide](https://azure.microsoft.com/en-us/documentation/articles/backup-azure-vms-troubleshoot/)
