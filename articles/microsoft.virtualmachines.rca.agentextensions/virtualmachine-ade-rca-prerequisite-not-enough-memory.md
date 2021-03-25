<properties
	pageTitle="Azure Disk Encryption RCA"
	description="RCA - ADE on Linux failing due to prerequisites"
	infoBubbleText="Found recent Azure Disk Encryption failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="summertgu"
	ms.author="tiag"
	displayOrder=""
	articleId="ADE_RCA-ade-on-linux-failing-prerequisites-not-enough-memory"
	diagnosticScenario="ADEFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="linux"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The operation on the Azure Disk Encryption for Linux extension on your virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because you don't have enough memory for encrypting the VM.
<!--/issueDescription-->
To avoid this issue, check the [supported VMs and operating systems](https://docs.microsoft.com/azure/virtual-machines/linux/disk-encryption-overview#supported-vms-and-operating-systems) to make sure your setup needs to comply with all the prerequisites.

## Resources
*See the full list of the requirements:*<br>

* [Azure Disk Encryption for Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/disk-encryption-overview)<br>
* [Azure Disk Encryption prerequisites for virtual machines and virtual machine scale sets](https://docs.microsoft.com/azure/security/azure-security-disk-encryption-prerequisites)
