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

4 out of 5 customers resolved their VM resize issue using the steps below.<br>

## **Recommended Steps**

## **Recommended steps**

We are experiencing capacity issues for specific regions across the globe. More details can be found by following this link to understand [Our commitment to customers and Microsoft cloud services continuity](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/)<br>

If you are deploying to regions **West Europe, North Europe, UK South, UK West, France Central**, then please be aware that we have an emerging issue related to capacity due to increased usage. In these cases, we recommend trying alternate regions (as first preference) or alternate SKUs.<br>

For general troubleshooting, please follow these steps:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region.<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))


## **Recommended Documents**

* [Troubleshoot deploying Linux virtual machine issues in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/restart-resize-error-troubleshooting)<br>
* [Classic Deployments: Troubleshoot allocation failures](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure-classic)<br>
* [Learn about the Virtual Machine lifecycle and states](https://docs.microsoft.com/azure/virtual-machines/linux/states-lifecycle)
