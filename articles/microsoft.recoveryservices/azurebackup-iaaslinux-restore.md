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

- Replacing an existing virtual machine during restore is not supported. You can use one of the following restore options

	- [Replace disks of existing backed-up VM](https://aka.ms/VMRestore-ReplaceExisting-disks)
	- [Resotre disks](https://aka.ms/VMrestore-restore-disk) and create a new VM using [Templates](https://aka.ms/templates-to-customize-a-restored-vm) or [Powershell](https://aka.ms/AB-AA4e56j)
	- [Restore as a new VM](https://aka.ms/AzureBackup-Restore-NewVM)

- Restore across subscription/region/zone is not supported for more info check [supported scenarios](https://aka.ms/VMBackup-Support-VMManagement) for VM management<br>
- If you are **unable to restore**, verify that you don’t have any group policy restriction in place from portal <br>
- If you are facing issues restoring a virtual machine, Try [Resotre disks](https://aka.ms/VMrestore-restore-disk) and create a new VM using [Templates](https://aka.ms/templates-to-customize-a-restored-vm) or [Powershell](https://aka.ms/AB-AA4e56j)<br>
- Files/Folders restore limitation on having special configuration [**Dynamic Disks or LVM/RAID Arrays**](https://aka.ms/AB-AA4ecqw) <br>
- To perform a restore ensure you have appropriate [Role Based Access controls in place](https://aka.ms/AB-AA4ecqc) <br>
- If you are **unable to see backup items** from the portal then ensure you have [required permission](https://aka.ms/AB-AA4ecq6) to access backup vault <br>
- To restore a VM into a specific availability set, restore disks and create a VM in availability sets using PowerShell cmdlets <br>
- In case of Azure Datacenter Disaster, Azure Backup [restores VM in paired data center](https://aka.ms/AB-AA4e56v)<br>
- We recommend using SSH based authentication for Linux VMs. If You are using Password based authentication on the VM which got backed up, you need to [reset password](https://aka.ms/AB-AA4e56u) post restore using VM Access extension <br>
- Restore disks will restore all disks (OS and data disks attached to the VM). Individual disk restore is not available using this option <br>
- If backed-up VM has special configuration then check [Restore VMs with special configurations](https://aka.ms/AB-AA4e56v) article<br>
- [Azure Virtual Machine restore troubleshooting guide](https://aka.ms/AB-AA4ecqi)
