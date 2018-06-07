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
Before filing support request validate below steps (these can potentially help resolve your issue): <br>

* Ensure your [**Windows VM Agent**](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows#manual-installation) is up to date if auto upgrate is disabled.<br> 

* Ensure there is [**connectivity**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-vm-has-no-internet-access) between VM and Azure Storage endpoints <br>   

* Backup can fail due to Snapshot extension issues, [**uninstall the extension to force reload**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load) and retry the operation <br> 

* Ensure the VM [**Windows OS version is compatible**](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#supported-operating-systems-for-backup) for using Azure Backup (versions older than Windows Server 2008 R2 are not supported) <br>   

## **Recommended documents**
* [VM agent is unable to communicate with the Azure Backup Service?](https://aka.ms/iaasvmbackuptshoot1) <br>
* [Snapshot operation failed due to no network connectivity on the virtual machine?](https://aka.ms/iaasvmbackuptshoot2) <br>
* [VMSnapshot extension operation failed?](https://aka.ms/iaasvmbackuptshoot3) <br>
* [Unable to perform the operation as the VM Agent is not responsive?](https://aka.ms/iaasvmbackuptshoot4) <br>
