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
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an allocation failure

<!--issueDescription-->
We detected that the operation **<!--$OperationType-->operationType<!--/$OperationType-->** operation for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an allocation failure.<br>
<!--/issueDescription-->

The hardware cluster where the availability set **<!--$avsetname-->myAvailabilitySet<!--/$avsetname-->** is hosted did not have enough capacity to support its allocation.<br>

An Azure Availability Set is created on a specific hardware cluster based upon the first VM using it. Each subsequent VM added must be compatible with the VM sizes supported in that hardware cluster. By having this constraint, high availability is maintained. In this case, the hardware cluster where the availability set is hosted did not have enough capacity to allocate the requested VM size.<br>

## **Recommended Steps**

We apologize for the inconvenience. Please try the <!--$OperationType-->operationType<!--/$OperationType--> operation on the VM again as the issue might have been temporary and there now could be sufficient resources for the allocation. If that doesn't work, you have the following options:<br>

- Deallocate all the VMs in the availability set, and then restart them again. Doing so enables the Azure platform to choose from more than one cluster when performing the allocation. The VM will use the same size that it had before the deallocation. 
- Resize the VM to a size that is currently available in your availability set. If you are using an older VM product, consider newer versions. See [Resize a Windows VM in an availability set](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm#resize-a-windows-vm-in-an-availability-set)<br>

For PowerShell examples for resizing a VM, for either in or not in an availability set, see [Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm).<br>

To determine available sizes using the Azure portal, select the VM and under **Settings**, choose **Size**. On the **Size** blade, you can view available sizes and use filter options.<br>

## **Recommended Documents**

- To determine sizes using PowerShell, use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command, for Azure CLI see the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command, for the REST API see the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.
- See [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/) for a conceptual overview on working with VM sizes, availability sets, availability zones, and regions.

