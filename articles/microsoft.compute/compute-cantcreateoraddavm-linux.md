<properties
	pageTitle="I can't create or add a VM"
	description="I can't create or add a VM"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder="20"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="linux, redhat, Ubuntu"
	productPesIds=""
	cloudEnvironments="public"
	articleId="70d17a56-e4bb-43e0-97cd-b80ab05efae6"
	ownershipId="Compute_VirtualMachines"
/>

# I can't create or add a VM

## **Recommended Steps**

We are experiencing high demand for specific regions across the globe. 4 out of 5 customers resolved their allocation failure issue using the below steps.

For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/).

## **Recommended Steps**

We are currently experiencing high demand in **West Europe, North Europe, UK South, UK West, and France Central**. If you are having availibility issues, please try alternate regions (as first preference) or alternate SKUs.

For general troubleshooting, please follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))
4. Review the different VM types in Azure. To resize, click 'Size' in the Settings blade of the VM resource:

To resolve most common issues, try one or more of the following steps:<br>

1. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to determine the failure reason<br>
2. Look up suggested actions by [Troubleshoot error codes for creating or adding a new VM](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/#error-string-lookup)<br>
3. Try your request using a smaller VM size or a different cloud service. [Configure regional Virtual Network to connect Cloud services](https://azure.microsoft.com/blog/vnet-to-vnet-connecting-virtual-networks-in-azure-across-different-regions/)<br>
4. If you're creating a new VM by using a custom image, review [How to capture a Linux virtual machine to use as a Resource Manager template](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-capture-image-resource-manager/)<br>

## **Recommended Documents**

* [Troubleshooting allocation failure when you create, restart or resize a VM in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/)
