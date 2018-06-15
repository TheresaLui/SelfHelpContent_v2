<properties
	pageTitle="Azure IAAS VM Backup Configure Protection"
	description="Azure IAAS VM Backup Configure Protection failures"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="kasparks"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553285"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Unable to Configure Backup for Azure  Virtual Machines?
## **Recommended steps**

- From Services.msc, ensure 'Windows Azure Guest Agent' services is 'Running'. <br>
- If 'Windows Azure Guest Agent' service is missing, then [install](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#install-the-vm-agent-on-the-virtual-machine). <br>
- [VM with more than 16 disks are not supported] (https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#limitations-when-backing-up-and-restoring-a-vm). <br>
- [Only Windows/Linux OS listed here support Backup](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#supported-operating-systems-for-backup). <br>
- [Ensure you have appropriate Role Based Access controls in place](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault). <br>

## **Recommended documents**
[Azure virtual machine backup troubleshooting guide'](https://azure.microsoft.com/documentation/articles/backup-azure-vms-troubleshoot/)
