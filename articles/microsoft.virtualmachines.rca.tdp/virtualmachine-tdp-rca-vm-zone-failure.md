<properties
	pageTitle="Operation Failure RCA"
	description="RCA - VM size not in zone"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="OperationFailure_RCA-VMSizeValidation-ZoneAllocationFailure"
	diagnosticScenario="OperationFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We detected that the start operation for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the availability zone **<!--$zonenumber--> <!--/$zonenumber-->** does not have the capacity to support its allocation.<br>
<!--/issueDescription-->

The availability zone has insufficient capacity to allocate the VM. Availability Zones are physically separate locations within an Azure region that provide high availability to protect your applications and data from datacenter failures.  

## **Recommended Steps**

Try the deployment again as the issue may have been temporary and there are now sufficient resources for the allocation. If that doesn't work, you have the following options:

- You can resize the VM. If you are using an older VM product, consider a newer versions. to another size and at any time you can contact us over a service request with a high severity and we will contact you to help you as soon as possible.
- Create a new VM for the availability zone. See [Create a Windows virtual machine in an availability zone with PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/create-powershell-availability-zone).
- Choose a size supported in an Azure Availability Set.<br>
- Choose a size supported in your region or in another region.<br>

To determine available sizes, select the VM in the Azure portal. Under **Settings**, choose **Size**. On the **Size** blade, you can view available sizes and use filter options.

## **Recommended Documents**

### Resizing

- See [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/) for considerations on working with VM sizes, availability sets, availability zones, and regions.
- Peruse [Products available by region](https://azure.microsoft.com/global-infrastructure/services/?products=virtual-machines) to see which products are available in all the regions.
- See [Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) for to resize a VM for an availability set using PowerShell.

### Size and SKU commands

- For PowerShell, Use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command and filter for a region:<br>`Get-AzComputeResourceSku` &vert; `where {$_.Locations.Contains("<<insert-region>>")}`

- For Azure CLI, Use the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command with the `--location` parameter to filter for a region and the `--size` parameter to match the size name:<br>`az vm list-skus --location <<insert-region>> --size <<insert-size>> --output table`

- For REST API, use the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.

