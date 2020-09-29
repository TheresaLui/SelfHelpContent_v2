<properties
	pageTitle="Allocation Failure RCA"
	description="AllocationFailed Create Update VM in avaiability set"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="AllocationFailure_RCA-create-update-avset"
	diagnosticScenario="AllocationFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your resource and found an allocation failure

<!--issueDescription-->
We detected that the **<!--$OperationType-->operationType<!--/$OperationType-->** operation for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an allocation failure.<br>
<!--/issueDescription-->

The hardware cluster where the availability set **<!--$avsetname-->myAvailabilitySet<!--/$avsetname-->** is hosted did not have enough capacity to support your allocation request.<br>

An Azure Availability Set is created on a specific hardware cluster based upon the first VM using it. Each subsequent VM added must be compatible with the VM sizes supported in that hardware cluster. By having this constraint, high availability is maintained. In this case, the hardware cluster where the availability set is hosted did not have enough capacity to allocate the requested VM size.<br>

## **Recommended Steps**

We apologize for the inconvenience. Please try the **<!--$OperationType-->operationType<!--/$OperationType-->** operation on the VM again as the issue might have been temporary and there now could be sufficient resources for the allocation. If that doesn't work, you have the following options:<br>

- Stop all the VMs in the availability set, update them to the desired size, and start them again. This deallocates the VMs in Azure and enables the Azure platform to choose from all available clusters when performing the first allocation request for the Start operation. 
- Resize the VM to a smaller size that is currently supported by the hardware cluster of your availability set. If you are using an older VM product, consider newer versions. You can use the Azure CLI command [az-vm-list-vm-resize-options](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-vm-resize-options) to check for available vm sizes. See [Resize a Windows VM in an availability set](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm#resize-a-windows-vm-in-an-availability-set) for additional information.<br>
- Recreate the VM in a new availability set. See [Change the availability set](https://docs.microsoft.com/azure/virtual-machines/windows/change-availability-set) for additional information.<br>

To determine supported sizes using the Azure portal, select the VM and under **Settings**, choose **Size**. On the **Size** blade, you can view supported sizes and use filter options. It should be noted that a VM size being supported in a cluster, does not mean that the cluster has enough capacity to allocate the VM.<br>

## **Recommended Documents**

- To determine sizes available in the region using PowerShell, use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command, for Azure CLI see the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command, for the REST API see the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.
- See [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/) for a conceptual overview on working with VM sizes, availability sets, availability zones, and regions.

