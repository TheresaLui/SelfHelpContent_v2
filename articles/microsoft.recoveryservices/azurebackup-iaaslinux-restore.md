<properties
	pageTitle="Azure Linux VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
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

- **Replacing an existing virtual machine during restore is not supported**. Please create a new virtual machine from backup or you can also restore disks from backup and use disks and configuration to create a new VM. Using [Portal](https://aka.ms/AB-AA4ecqv), Using [PowerShell](https://aka.ms/AB-AA4e566), from [restored disk](https://aka.ms/AB-AA4ecqq) <br>
- If you are facing issues restoring a virtual machine, please try *Restore Disk* functionality: <br>
  - **Step 1** - [*Restore Disks*](https://aka.ms/AB-AA4e570) functionality. <br>
  - **Step 2** - Use the disk that was restored to [*create a virtual machine*](https://aka.ms/AB-AA4e56j).<br>
- **Cross region and cross-subscription restore is not supported** i.e. if your VM which got backed up is in West Europe, you can only restore to West Europe in same subscription.<br>
- If you are **unable to restore**, verify that you don’t have any group policy restriction in place from portal.<br>
- If you are **unable to see backup items** from the portal then ensure you have [required permission](https://aka.ms/AB-AA4ecq6) to access backup vault. <br>
- [File/Folder restore limitation with special configuration - **Dynamic Disks, LVM/RAID Arrays**](https://aka.ms/AB-AA4ecqw) <br>
- [Ensure you have appropriate Role Based Access controls in place](https://aka.ms/AB-AA4ecqc) <br>
- We recommend using SSH based authentication for Linux VMs. If You are using Password based authentication on the VM which got backed up, you need to [reset password](https://aka.ms/AB-AA4e56u) post restore using VM Access extension. <br>
- To Restore a VM into a specific availability set, restore disks and configuration, and create a VM use PowerShell cmdlets. [Learn More](https://aka.ms/AB-AA4e56z) <br>
- In case of Azure Datacenter Disaster, Azure Backup [restores VM in paired data center](https://aka.ms/AB-AA4e56v) <br>
- Restore disks will restore all disks(OS and data disks attached to the VM). Individual disk restore is not possible using this option. <br>
- [Azure virtual machine restore troubleshooting guide](https://aka.ms/AB-AA4ecqi)<br>
