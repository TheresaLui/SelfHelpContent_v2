<properties
	pageTitle="My desired region or VM size is unavailable"
	description="My desired region or VM size is unavailable"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32628263"
	resourceTags=""
	productPesIds="15571, 15797, 16454,16470"
	cloudEnvironments="public, Fairfax"
	articleId="9c65e013-d2bf-4376-87cd-b34554d71bf7"
	ownershipId="Compute_VirtualMachines"
/>

# My desired region or VM size is unavailable

>We are currently experiencing high demand for specific regions across the globe. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/).<br>

## **Recommended Steps**

>If you are having availability issues in **West Europe, North Europe, UK South, UK West, and France Central**, please try alternate regions (as first preference) or alternate SKUs.<br>

For general troubleshooting, please follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))

## **Recommended Documents**

* [Understanding SkuNotAvailable - Some SKU series are unavailable for the selected subscription for this region](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors)<br>
* [Resolve errors associated with quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors)<br>
* [Troubleshoot allocation failures when you create, restart, or resize VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)<br>
* [Resizing a VM or add VMs to an existing availability set](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure#resize-a-vm-or-add-vms-to-an-existing-availability-set)<br>
* [Troubleshoot allocation failures when creating a new virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-allocation-failure)<br>
* [Troubleshoot deployment issues when creating a new virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-troubleshoot-deployment-new-vm)
