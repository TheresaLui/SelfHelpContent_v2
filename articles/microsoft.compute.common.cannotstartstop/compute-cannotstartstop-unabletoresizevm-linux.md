<properties
	pageTitle="I am unable to resize my VM"
	description="I am unable to resize my VM"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure,timbasham"
	ms.author="scotro,tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32628260"
	resourceTags=""
	productPesIds="15571,15797,16454,16470"
	cloudEnvironments="public, Fairfax"
	articleId="b112665b-c56a-41d0-96ff-8ffe3cacd25b"
	ownershipId="Compute_VirtualMachines"
/>

# I am unable to resize my VM

## **Awareness**

>We are currently experiencing high demand for specific regions across the globe. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://aka.ms/CloudCovidResponseFAQ).<br>

## **Recommended Steps**

>If you are experiencing allocation failures in **West Europe, North Europe, UK South, UK West, and France Central**, please try alternate regions (as first preference) or alternate SKUs.<br>

For general troubleshooting, please follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))

## **Recommended Documents**

* [Troubleshoot deploying Linux virtual machine issues in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/restart-resize-error-troubleshooting)<br>
* [Classic Deployments: Troubleshoot allocation failures](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure-classic)<br>
* [Learn about the Virtual Machine lifecycle and states](https://docs.microsoft.com/azure/virtual-machines/linux/states-lifecycle)
