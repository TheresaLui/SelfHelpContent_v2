<properties
	pageTitle="Allocation Failure RCA"
	description="AllocationFailed create standalone VM"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachinescalesets"
	authors="summertgu"
	ms.author="tiag"
	displayOrder=""
	articleId="VMSS_AllocationFailure_RCA-create-standalone"
	diagnosticScenario="AllocationFailure"
	selfHelpType="rca"
	supportTopicIds="32641079,32641082,32641076,32641075,32641080,32641074,32641076,32641077,32641072,32641073"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public, Fairfax"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# We ran diagnostics on your resource and found an allocation failure

<!--issueDescription-->
We detected that a **<!--$OperationType-->operationType<!--/$OperationType-->** operation for virtual machine scale set **<!--$vmssname-->Virtual machine scale set<!--/$vmssname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an allocation failure.<br>
<!--/issueDescription-->

The region this VM scale set is associated with did not have enough capacity at the time to support its allocation.<br>

## **Recommended Steps**

We apologize for the inconvenience. Please try creating the VM scale set again as the issue might have been temporary and there now could be sufficient resources for the allocation. If that doesn't work, consider choosing another VM size that is currently available in your region. If you are using an older VM product, consider newer versions.<br>

To search and browse the virtual machine scale sets by region, choose `virtual machine scale sets` in an interactive query that Azure provides [here](https://azure.microsoft.com/global-infrastructure/services/?products=virtual-machine-scale-sets).<br>

## **Recommended Documents**

- To determine sizes available in the region using PowerShell, use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command, for Azure CLI see the [az vmss list-skus](https://docs.microsoft.com/cli/azure/vmss?view=azure-cli-latest#az-vmss-list-skus) and [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) commands, for the REST API see the [Virtual Machine Scale Sets - List Skus](https://docs.microsoft.com/rest/api/compute/virtualmachinescalesets/listskus) and [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operations
- For a conceptual overview on working with VM sizes, availability sets, availability zones, and regions, see [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/)
