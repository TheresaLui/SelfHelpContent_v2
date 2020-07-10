<properties
	pageTitle="Allocation Failure RCA"
	description="AllocationFailed Start on VM in standalone VM or in AV set"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="AllocationFailure_RCA-start-standalone-avset"
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
We detected that the start operation for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an allocation failure.<br>
<!--/issueDescription-->

The hardware cluster where the VM is hosted did not have enough capacity to start the VM.<br>

## **Recommended Steps**

We apologize for the inconvenience. Please try starting the VM again as the issue might have been temporary and there now could be sufficient resources for the allocation. If that doesn't work, you have the following options:<br>

- If the VM is an availability set, deallocate all the VMs in the availability set  and then restart them again. Doing so enables the Azure platform to choose from more than one cluster when performing the allocation. The VM will use the same size that it had before the deallocation. 
- Resize the VM to a size that is currently available in your region. If you are using an older VM product, consider newer versions.<br>

For PowerShell examples to resize a VM, for both in an availability set and not in availability set, see [Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm).<br>

To determine available sizes using PowerShell, use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command, for Azure CLI see the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command, for the REST API see the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.<br>

To determine available sizes using the Azure portal, select the VM and under **Settings**, choose **Size**. On the **Size** blade, you can view available sizes and use filter options.

