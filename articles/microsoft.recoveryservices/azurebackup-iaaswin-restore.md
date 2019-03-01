<properties
	pageTitle="Azure Windows VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	ms.author="trinadhk"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32553299"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
	articleId="6fff7f67-d153-43f0-89c9-598eba2fe465"
/>

# Azure Windows VM Restore Limitations

## **Recommended Steps**

**Frequently Asked Questions:**

- [How can I restore specific files or folders from Azure Virtual Machine?](https://aka.ms/AB-AA4e56a)<br>
- Restore to latest/specific recovery point using:
	- [Portal](https://aka.ms/AB-AA4ecqx)
	- [PowerShell](https://aka.ms/AB-AA4e56o) 
	- [Restored disk](https://aka.ms/AB-AA4ecqq)<br>
	
- [Configure static IP address to restored VM](https://aka.ms/AB-AA4e56r)<br>
- [Restore an Encrypted VM](https://aka.ms/AB-AA4e56t)<br>
- [Restore when KEK (Key Encryption Key) and BEK (BitLocker Encryption Key) does not exist in the key vault?](https://aka.ms/AB-AA4ecqr)<br>
- [How to restore a Domain Controller VM?](https://aka.ms/AB-AA4e56v)<br>
- How can I attach existing NIC to the restored VM?
	1. [Remove from original VM](https://aka.ms/AB-AA4ecr0)
	2. [Attach to restored VM](https://aka.ms/AB-AA4e56s)
	
- [Restore VM with special network configurations?](https://aka.ms/AB-AA4e56w)<br>

**Limitations**<br>

- Restoring backed-up VMs across Zone, Region, subscription or V-Net is not supported <br>
- [File/Folder restore limitation with special configuration - **Dynamic Disks, Storage Spaces**](https://aka.ms/AB-AA4ecqw) <br>

**Common Errors and Workarounds**<br>

- If you are **unable to restore**, verify that you don’t have any group policy restriction in place from portal
- If you are **unable to see backup items** from the portal then ensure you have [required permission](https://aka.ms/AB-AA4ecqc) to access backup vault
- [Ensure appropriate Role Based Access controls in place](https://aka.ms/AB-AA4ecqc) <br>
- [Restore failed with Cloud Internal error](https://aka.ms/AB-AA4ecqi)<br>
- [The selected DNS name is already taken](https://aka.ms/AB-AA4ecqi)<br>
- [The specified virtual network configuration is not correct](https://aka.ms/AB-AA4ecqi)<br>
- [The specified cloud service is using a reserved IP]https://aka.ms/AB-AA4ecqi)<br>

## **Recommended Documents**

- [Azure Virtual Machine restore troubleshooting guide](https://aka.ms/AB-AA4ecqi)<br>
- [How to restore virtual machine using portal](https://aka.ms/AB-AA4e565)<br>
- [How to restore virtual machine using PowerShell](https://aka.ms/AB-AA4e56z)<br>
