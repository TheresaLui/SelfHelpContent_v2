<properties
	pageTitle="Allocation Failure RCA"
	description="AllocationFailed update start standalone VM"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="AllocationFailure_RCA-update-start-standalone"
	diagnosticScenario="AllocationFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an allocation failure

<!--issueDescription-->
We detected that the **<!--$OperationType-->operationType<!--/$OperationType-->** operation for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an allocation failure.<br>
<!--/issueDescription-->

The hardware cluster where the VM is deployed did not have enough capacity at the time to support its allocation.<br>

## **Recommended Steps**

We apologize for the inconvenience. Please try the operation again as the issue might have been temporary and there now could be sufficient resources for the allocation. If that doesn't work, you have the following options:<br>

- Deallocate the VM, and then start it again. Deallocating the VM enables the Azure platform to choose from more than one cluster when performing the allocation. The VM will use the same size that it had before the deallocation.
- Deallocate the VM, and choose a size that is supported in the region. See the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.
- Resize the VM to a different size that is supported in the current hardware cluster. See [Resize a Windows VM not in an availability set](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/resize-vm#resize-a-windows-vm-not-in-an-availability-set).<br>

To search and browse the virtual machines by region, choose `virtual machines` in an interactive query that Azure provides [here](https://azure.microsoft.com/global-infrastructure/services/?products=virtual-machines). It should be noted that a VM size being supported in a cluster/region, does not mean that the cluster/region has enough capacity to allocate the VM.<br>

## **Recommended Documents**

- To determine sizes using PowerShell, use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command, for Azure CLI see the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command, for the REST API see the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation
- For a conceptual overview on working with VM sizes, availability sets, availability zones, and regions, see [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/)

