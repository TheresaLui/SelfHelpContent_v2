<properties
	pageTitle="I can't restart or resize an existing VM"
	description="I can't restart or resize an existing VM"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder="25"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="windows, linux, windowsSQL, redhat, Ubuntu"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1cf1dd0b-8bde-4432-a753-6e800568aa29"
	ownershipId="Compute_VirtualMachines"
/>

# I can't restart or resize an existing VM

## **Awareness**

>We are currently experiencing high demand for specific regions. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://aka.ms/CloudCovidResponseFAQ).<br>

## **Recommended Steps**

>If you are experiencing allocation failures in **UAE North**, please try alternate regions (as first preference) or alternate SKUs.<br>

For general troubleshooting, please follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region.<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))

## **Recommended Documents**

* [Configure regional Virtual Network to connect Cloud services](https://azure.microsoft.com/blog/vnet-to-vnet-connecting-virtual-networks-in-azure-across-different-regions/)<br>
* [Troubleshooting allocation failure when you create, restart or resize a VM in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/)
