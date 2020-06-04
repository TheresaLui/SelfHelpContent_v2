<properties
	pageTitle="Virtual Machine Size Not Found RCA"
	description="Virtual Machine Size Not Found - Standalone"
	infoBubbleText="Found diagnostic result for the selected resource. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro,rashan"
	displayOrder=""
	articleId="SupportTopic_RCA-sizenotfound-standalone-nondeallocated"
	diagnosticScenario="SizeNotFoundStandalone-NonDeallocated"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your resource

<!--issueDescription-->
We detected that the virtual machine **<!--$vmname-->myVM<!--/$vmname-->** is deployed in region **<!--$region-->region<!--/$region-->** without any availability constraints, and the power state of the VM is **<!--$powerstate-->powerstate<!--/$powerstate-->**.<br>
<!--/issueDescription-->

An Azure region is partitioned into several hardware clusters. When the power state of the VM is **Running**, **Starting**, **Stopped**, or **Stopping**, the VM is deployed and hosted on a specific hardware cluster. 

When the VM is in such a state, resize options are **specifically limited** to sizes available on the current hardware cluster.

## **Recommended Steps**

We apologize for the inconvenience. If you are unable to find the VM size that you are looking for, you have the following options:<br>

- Stop the VM, update it to the desired size, and start it again. This deallocates the VM in Azure and enables the Azure platform to choose from all available clusters when deploying the VM. To see the list of available VM sizes upfront before deallocating, you can use the Azure CLI command [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus).
- Resize the VM to a size that is currently supported by the hardware cluster of your availability set. If you are using an older VM product, consider newer versions. You can use the Azure CLI command [az-vm-list-vm-resize-options](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-vm-resize-options) to check for available vm sizes.<br>

To see the list of sizes that are available for deployment for subscription **<!--$SubscriptionID-->SubscriptionID<!--/$SubscriptionID-->**, you can use the Azure CLI command [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) to check for the VM sizes available in a region, and any deployment restrictions on the VM size. If the size you desire is not listed, or is marked **NotAvailableForSubscription**, please follow the steps in [Troubleshooting region or SKU subscription issues](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable) to submit a streamlined request for accessing the SKU size.

## **Recommended Documents**

- To determine sizes available for your subscription using PowerShell, use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command, for Azure CLI see the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command, for the REST API see the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.
- See [Virtual machines lifecycle and states](https://docs.microsoft.com/azure/virtual-machines/windows/states-lifecycle) for an overview of VM power states and lifecycle.
- See [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/) for a conceptual overview on working with VM sizes, availability sets, availability zones, and regions.
