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
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="a5788e7e-192d-4885-b271-ffa4423fae91"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>

## **Awareness**

>We are currently experiencing high demand for specific regions. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://aka.ms/CloudCovidResponseFAQ).<br>

## **Recommended Steps**

>If you are experiencing allocation failures in **UAE North**, please try alternate regions (as first preference) or alternate SKUs.<br>

For general troubleshooting, please follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))

## **Recommended Documents**

* [Frequently Asked Questions (FAQ) for VMSS](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-faq)<br>
* [Troubleshoot FAQ for VMSS](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-faq#troubleshooting)<br>
* [Best practices for Azure AutoScale](https://docs.microsoft.com/azure/monitoring-and-diagnostics/insights-autoscale-best-practices)
