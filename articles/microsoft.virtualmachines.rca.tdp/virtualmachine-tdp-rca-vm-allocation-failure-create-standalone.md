<properties
	pageTitle="Allocation Failure RCA"
	description="AllocationFailed create standalone VM"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="AllocationFailure_RCA-create-standalone"
	diagnosticScenario="AllocationFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an allocation failure

<!--issueDescription-->
We detected that a create operation for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an allocation failure.<br>
<!--/issueDescription-->

The region this VM is associated with did not have enough capacity at the time to support its allocation.<br>

## **Recommended Steps**

We apologize for the inconvenience. Try creating the VM as the issue might have been temporary and there now could be sufficient resources for the allocation. If that doesn't work, consider choosing another VM size that is currently available in your region. If you are using an older VM product, consider newer versions. 

See [Products by region](https://azure.microsoft.com/regions/services/) to search and browse for products by region and [Resize a Windows VM not in an availability set](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm#resize-a-windows-vm-not-in-an-availability-set).

### Request exemption

If you are unable to find suitable alternate locations or VM sizes and would like to submit a request for an SKU to be enabled, follow the support request process described in [Region or SKU unavailable](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable). This action will streamline your request and assist in getting a faster turnaround time.<br>

## **Recommended Documents**

- To determine sizes using PowerShell, use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command, for Azure CLI see the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command, for the REST API see the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.
- For a conceptual overview on working with VM sizes, availability sets, availability zones, and regions, see [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/). 

