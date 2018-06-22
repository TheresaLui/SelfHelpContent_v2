<properties
	pageTitle="Backup of Windows Azure virtual machine fails"
	description="Top issues causing Windows Azure virtual machine backup failures"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32553277"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Backup of Windows Azure virtual machine fails

## **Recommended steps**
- [Ensure your Windows VM agent is up to date before troubleshooting further](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows#manual-installation) <br>
- [Ensure there is connectivity between VM and Azure Storage endpoints](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-vm-has-no-internet-access) <br>
- [For Snapshot extension issues, uninstall extensions to force reload & retry backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load) <br>
- [OS Versions older than Windows Server 2008 R2 are not supported for Backup](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#supported-operating-systems-for-backup) <br>

## **Recommended documents**
- [VM agent is unable to communicate with the Azure Backup Service?](https://aka.ms/iaasvmbackuptshoot1) <br>
- [Snapshot operation failed due to no network connectivity on the virtual machine?](https://aka.ms/iaasvmbackuptshoot2) <br>
- [VMSnapshot extension operation failed?](https://aka.ms/iaasvmbackuptshoot3) <br>
- [Unable to perform the operation as the VM Agent is not responsive?](https://aka.ms/iaasvmbackuptshoot4) <br>
