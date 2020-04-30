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
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="37f0fdfb-3b67-4b90-b692-c0db770af827"
	ownershipId="Compute_VirtualMachines_Content"
/>

# My desired region or VM size is unavailable

## **Awareness**

>We are currently experiencing high demand for specific regions. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://aka.ms/CloudCovidResponseFAQ).<br>

## **Recommended Steps**

>If you are experiencing allocation failures in **UAE North**, please try alternate regions (as first preference) or alternate SKUs.<br>

For general troubleshooting, please follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))

## **Recommended Documents**

* [Understanding SkuNotAvailable - Some SKU series are unavailable for the selected subscription for this region](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors)<br>
* [Resolve errors associated with quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors)<br>
* [Troubleshoot allocation failures when you create, restart, or resize VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)<br>
* [Resizing a VM or add VMs to an existing availability set](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure#resize-a-vm-or-add-vms-to-an-existing-availability-set)<br>
* [Troubleshoot deployment issues when creating a new virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-troubleshoot-deployment-new-vm)<br>
* [Troubleshoot allocation failures when creating a new virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-allocation-failure)
* [Azure confidential computing VM Sizes](https://docs.microsoft.com/azure/confidential-computing/virtual-machine-solutions#azure-confidential-computing-vm-sizes)
