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
	resourceTags="windows,windowsSQL"
	productPesIds=""
	cloudEnvironments="public"
	articleId="3201a2b8-d746-4136-8c87-efba94789b12"
	ownershipId="Compute_VirtualMachines"
/>

# I can't create or add a VM

>We are currently experiencing high demand for specific regions across the globe. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/).<br>

## **Recommended Steps**

>If you are having availability issues in **West Europe, North Europe, UK South, UK West, and France Central**, please try alternate regions (as first preference) or alternate SKUs.<br>

For general troubleshooting, please follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))<br>
4. Review the different VM types in Azure. To resize, click 'Size' in the Settings blade of the VM resource.

To resolve common issues, try one or more of the following methods:<br>

1. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to determine the failure reason
2. [Troubleshoot error codes for create or add a new VM](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/#error-string-lookup)
3. Try your request using a smaller VM size or different cloud service: [Configure regional Virtual Network to connect Cloud services](https://azure.microsoft.com/blog/vnet-to-vnet-connecting-virtual-networks-in-azure-across-different-regions/)<br>
4. If you're creating a new VM using a custom image, review [How to capture a Windows virtual machine in the Resource Manager deployment model](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-capture-image-resource-manager/)<br>

## **Recommended Documents**

* [Troubleshooting allocation failure when you create, restart or resize a VM in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/)
