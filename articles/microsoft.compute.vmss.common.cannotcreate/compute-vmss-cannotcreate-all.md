<properties
	pageTitle="Cannot create a new scale set"
	description="Cannot create a new scale set"
	service="microsoft.compute"
	resource=""
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32641072"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public, Fairfax"
	articleId="a5788e7e-192d-4885-b271-ffa4423fae91"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>

# Cannot create a new scale set

4 out of 5 customers resolved their VMSS issue using the below documents.<br>

## **Recommended Steps**

We are experiencing capacity issues for specific regions across the globe. More details can be found by following this link to understand [Our commitment to customers and Microsoft cloud services continuity](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/)<br>

If you are deploying to regions **West Europe, North Europe, UK South, UK West, France Central**, then please be aware that we have an emerging issue related to capacity due to increased usage. In these cases, we recommend trying alternate regions (as first preference) or alternate SKUs.<br>

For general troubleshooting, please follow these steps:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region.<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))

## **Recommended Documents**

* [Frequently Asked Questions (FAQ) for VMSS](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-faq)<br>
* [Troubleshoot FAQ for VMSS](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-faq#troubleshooting)<br>
* [Best practices for Azure AutoScale](https://docs.microsoft.com/azure/monitoring-and-diagnostics/insights-autoscale-best-practices)
