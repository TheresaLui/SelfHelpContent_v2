<properties
	pageTitle="Azure Linux VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds="32553297"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
	articleId="9344f1ee-97c8-459c-8a55-58c514b4d2ef"
/>

# Azure Linux VM Restore Limitations

## **Recommended Steps**

**Limitations**

- Restoring backed-up VMs across Zone/Region/subscription or V-Net is not supported. For more info check [supported scenarios](https://aka.ms/VMBackup-Support-VMManagement) for VM management<br>
- Files/Folders restore limitation on having special configuration [**Dynamic Disks or LVM/RAID Arrays**](https://aka.ms/AB-AA4ecqw) <br>
- Restore disks will restore all disks (OS and data disks attached to the VM). Individual disk restore is not available using this option <br>
- Replacing an existing virtual machine during restore is not supported. You can use one of the following restore options

	- [Replace disks of existing backed-up VM](https://aka.ms/VMRestore-ReplaceExisting-disks)<br>
	- [Restore disks](https://aka.ms/VMrestore-restore-disk) and create a new VM using [Templates](https://aka.ms/templates-to-customize-a-restored-vm) or [PowerShell](https://aka.ms/AB-AA4e56j)
	- [Restore as a new VM](https://aka.ms/AzureBackup-Restore-NewVM)
	
**Frequently Asked Questions**

- How to:
	- [Restore specific files or folders from Azure Virtual Machine backup?](https://aka.ms/AB-AA4e56a)<br>
	- Restore to latest/specific recovery point using [Portal](https://aka.ms/AB-AA4ecqx), [PowerShell](https://aka.ms/AB-AA4e56o)?
	- [Configure static IP address to restored VM?](https://aka.ms/AB-AA4e56r)<br>
	- [Restore an Encrypted VM?](https://aka.ms/AB-AA4e56t)<br>
	- [Restore when KEK (Key Encryption Key) and BEK (BitLocker Encryption Key) does not exist in the key vault?](https://aka.ms/AB-AA4ecqr)<br>
	- [Restore a Domain Controller VM?](https://aka.ms/AB-AA4e56v)<br>
	- [Restore VM with special configurations?](https://aka.ms/AB-AA4e56v)<br>
	- Attach an existing NIC to the restored VM?

	 Step 1: [Remove from original VM](https://aka.ms/AB-AA4ecr0)<br>
	 Step 2: [Attach to restored VM](https://aka.ms/AB-AA4e56s)<br>

**Recommendations**

- If you are **unable to restore**, verify that you don’t have any group policy restriction in place from portal
- We recommend using SSH based authentication for Linux VMs. If You are using Password based authentication on the VM which got backed up, you need to [reset password](https://aka.ms/AB-AA4e56u) post restore using VM Access extension <br>
- If you are **unable to see backup items** from the portal then ensure you have [required permission](https://aka.ms/AB-AA4ecqc) to access backup vault
- If you are facing issues restoring a virtual machine, Try [Restore disks](https://aka.ms/VMrestore-restore-disk) and create a new VM using [Templates](https://aka.ms/templates-to-customize-a-restored-vm) or [PowerShell](https://aka.ms/AB-AA4e56j)<br>
- To perform a restore ensure you have appropriate [Role Based Access controls in place](https://aka.ms/AB-AA4ecqc) <br>
- To restore a VM into a specific availability set, restore disks and create a VM in availability sets using PowerShell cmdlets <br>
- In case of Azure Datacenter Disaster, Azure Backup [restores VM in paired data center](https://aka.ms/AB-AA4e56v)<br>

## **Recommended Documents**

- [Azure Virtual Machine restore troubleshooting guide](https://aka.ms/AB-AA4ecqi)<br>
- [How to restore virtual machine using portal](https://aka.ms/AB-AA4e565)<br>
- [How to restore virtual machine using PowerShell](https://aka.ms/AB-AA4e56z)<br>
