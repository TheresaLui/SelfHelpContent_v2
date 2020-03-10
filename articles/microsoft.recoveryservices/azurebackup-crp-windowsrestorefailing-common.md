<properties
	pageTitle="Azure Backup - Restore is failing"
	description="Azure Backup - Restore is failing"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32637326"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public, Fairfax"
	articleId="4f74f61e-97d5-49ba-8caf-fc1f0d5c2792"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Azure Backup - Restore is failing

## **Recommended Steps**

**Known Limitations**

- Restoring backed-up VMs across Zone/Region/subscription or V-Net is not supported. For more information, see [supported scenarios](https://aka.ms/VMBackup-Support-VMManagement) for VM management.
- Files/Folders restore limitation on having special configuration [**Dynamic Disks or LVM/RAID Arrays**](https://aka.ms/AB-AA4ecqw)
- Restore disks will restore all disks (OS and data disks attached to the VM). Individual disk restore is not available using this option.
- Replacing an existing virtual machine during restore is not supported. You can use one of the following restore options:

	- [Replace disks of existing backed-up VM](https://aka.ms/VMRestore-ReplaceExisting-disks)<br>
	- [Restore disks](https://aka.ms/VMrestore-restore-disk) and create a new VM using [Templates](https://aka.ms/templates-to-customize-a-restored-vm) or [PowerShell](https://aka.ms/AB-AA4e56j)
	- [Restore as a new VM](https://aka.ms/AzureBackup-Restore-NewVM)

**Frequently Asked Questions**

- [Restore specific files or folders from Azure Virtual Machine backup](https://aka.ms/AB-AA4e56a)<br>
- Restore to latest or specific recovery point using [Portal](https://aka.ms/AB-AA4ecqx) or [PowerShell](https://aka.ms/AB-AA4e56o)
- [Configure static IP address to restored VM](https://aka.ms/AB-AA4e56r)<br>
- [Restore an Encrypted VM](https://aka.ms/AB-AA4e56t)<br>
- [Restore when KEK (Key Encryption Key) and BEK (BitLocker Encryption Key) does not exist in the key vault](https://aka.ms/AB-AA4ecqr)<br>
- [Restore a Domain Controller VM](https://aka.ms/AB-AA4e56v)<br>
- [Restore VM with special configurations](https://aka.ms/AB-AA4e56v)<br>
- Attach an existing NIC to the restored VM:

	- Step 1: [Remove from original VM](https://aka.ms/AB-AA4ecr0)<br>
	- Step 2: [Attach to restored VM](https://aka.ms/AB-AA4e56s)<br>

- If you are unable to restore, verify that you don’t have any group policy restriction from portal
- If you are unable to see **Backup Items** from the portal, ensure you have [required permission](https://aka.ms/AB-AA4ecqc) to access backup vault
- If you are facing issues restoring a VM, try [Restore disks](https://aka.ms/VMrestore-restore-disk) and create a new VM using [Templates](https://aka.ms/templates-to-customize-a-restored-vm) or [PowerShell](https://aka.ms/AB-AA4e56j)<br>
- To perform a restore ensure you have appropriate [Role Based Access Controls in place](https://aka.ms/AB-AA4ecqc) <br>
- To restore a VM into a specific availability set, [Restore disks](https://aka.ms/VMrestore-restore-disk) and create a VM in availability sets using PowerShell cmdlets <br>
- In case of Azure datacenter disaster, Azure Backup [restores VM in paired datacenter](https://aka.ms/AB-AA4e56v)<br>

## **Recommended Documents**

- [Azure Virtual Machine restore troubleshooting guide](https://aka.ms/AB-AA4ecqi)<br>
- [Restore Azure Virtual Machine using portal](https://aka.ms/AB-AA4e565)<br>
- [Restore Azure Virtual Machine using PowerShell](https://aka.ms/AB-AA4e56z)<br>
