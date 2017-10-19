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
To resolve common issues, try one or more of the following steps.

**VM agent is unable to communicate with the Azure Backup Service?** <br>
Follow these [troubleshooting steps](https://aka.ms/guestagent-status-unavailable) to resolve communication issues <br>

**Snapshot operation failed due to no network connectivity on the virtual machine?** <br>
Follow these [troubleshooting steps](https://aka.ms/extension-snapshot-failed-nonetwork) to resolve snapshot failure issues <br>

**VMSnapshot extension operation failed?**<br>
This issue may occur if extensions cannot be loaded, Backup fails because a snapshot cannot be taken.<br>
Follow these [troubleshooting steps](https://aka.ms/extension-operation-failed) to resolve extension operation failed issues.

**Backup failed with an internal error - Please retry the operation in a few minutes**<br>
Follow these [troubleshooting steps](https://aka.ms/backup-operation-failed) to resolve theses issues

**The specified Disk configuration is not supported** <Br>
This issue occurs if the Virtual Machine contains a disk [***greater than 1 TB***](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#limitations-when-backing-up-and-restoring-a-vm) <br>
Please follow below steps to [resolve](https://aka.ms/large-disk-support) this issue.
- If you have disks greater than 1 TB , [attach new disks](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal) which are less than 1 TB <br>
- Once you attach new disks which are less than 1TB, copy the data from disk greater than 1TB into newly created disk(s) of size less than 1TB. <br>
- Ensure that all data has been copied and remove the disks greater than 1TB
- Initiate the backup


## **Recommended documents**
[Azure virtual machine backup troubleshooting guide](https://azure.microsoft.com/documentation/articles/backup-azure-vms-troubleshoot/)<br>
