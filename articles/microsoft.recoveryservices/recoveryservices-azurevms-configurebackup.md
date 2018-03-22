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
To resolve the most common issues, try one or more of the following steps.<br>

**VM agent is unable to communicate with the Azure Backup Service?** <br>
This issue may occur if the VM Agent service is missing/not in running status (verify it from services.msc of your VM) in Azure Virtual Machine. Try to restart VM agent /[re-install](http://go.microsoft.com/fwlink/?LinkID=394789&clcid=0x409) it to resolve the issue <br>
Follow the [troubleshooting steps](https://aka.ms/guestagent-status-unavailable) to resolve such communication issues <br>

**Azure Backup does not support disk sizes greater than 1023GB?**<br>
This issue may occur if the virtual machine has the disk size [greater than 1 TB](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#limitations-when-backing-up-and-restoring-a-vm).<br>

We have a private preview to support backups for VMs with >1TB disks. For details refer to [Private preview for large disk VM backup support](https://gallery.technet.microsoft.com/Instant-recovery-point-and-25fe398a)<br>
If you do not wish to join the preview, follow below steps to resolve this issue : <br>

* If you have disks greater than 1 TB , [attach new disks](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal) which are less than 1 TB<br>
*	Then, copy the data from disk greater than 1TB into newly created disk(s) of size less than 1TB<br>
* Ensure that all data has been copied and remove the disks greater than 1TB<br>
* Initiate the backup <br>

For more information click [here](https://aka.ms/large-disk-support)<br>

**Unable to perform the operation as the VM Agent is not responsive?**<br>
This issue may occur if the VM Agent service is missing/not in running status (verify it from services.msc of your VM) in Azure Virtual Machine. Try to restart VM agent / [re-install](http://go.microsoft.com/fwlink/?LinkID=394789&clcid=0x409) it to resolve the issue <br>
Follow the [troubleshooting steps](https://aka.ms/guestagent-status-unavailable) to resolve most communication issues <br>

**Backup failed with an internal error - Please retry the operation in a few minutes. If the problem persists, contact Microsoft Support?**<br>
This issue may occur if the VM Agent service is missing/not in running status (verify it from services.msc of your VM) in Azure Virtual Machine. Try to restart VM agent / [re-install](http://go.microsoft.com/fwlink/?LinkID=394789&clcid=0x409) it to resolve the issue <br>
Follow the [troubleshooting steps](https://aka.ms/guestagent-status-unavailable) to resolve most communication issues <br>

## **Recommended documents**
[Azure virtual machine backup troubleshooting guide'](https://azure.microsoft.com/documentation/articles/backup-azure-vms-troubleshoot/)
