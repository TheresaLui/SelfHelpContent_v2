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
- [Ensure your Linux VM agent is up to date before troubleshooting further](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms)<br>
- [Ensure there is connectivity between VM and Azure Storage endpoints](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-vm-has-no-internet-access)<br>
- [If your Linux OS/Kernel version is not listed here, then it is not supported](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#supported-operating-systems-for-backup)<br>
- [For Snapshot extension issues, uninstall extensions to force reload & retry backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load)<br>
- [If your issue is still not resolved, check VM Backup troubleshooting guide](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout)<br>
