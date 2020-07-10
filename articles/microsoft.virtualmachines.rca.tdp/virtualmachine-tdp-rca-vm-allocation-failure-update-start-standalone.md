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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your resource and found an allocation failure

<!--issueDescription-->
We detected that the **<!--$OperationType-->operationType<!--/$OperationType-->** operation for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an allocation failure.<br>
<!--/issueDescription-->

The hardware cluster where the VM is currently deployed did not have enough capacity of this size to support your allocation request.<br>

## **Recommended Steps**

We apologize for the inconvenience. Please try the operation again as the issue might have been temporary and there now could be sufficient resources for this allocation. If that fails with the same error, then you have the following options:<br>

- Stop the VM, update it to the desired size in the region, and start it again. This deallocates the VM in Azure and enables the Azure platform to choose from all available hardware clusters when performing the allocation request for the Start operation. Please note that deallocating a VM will remove any data on the temp disk, and the public IP address will change unless a static IP address is being used.
- If you are unwilling to deallocate the VM, you can resize the VM to a different size that is supported in the current hardware cluster. See [az vm list-vm-resize-options](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-vm-resize-options) for resizing options.

Please refer to [Resize a VM](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-manage-vm#resize-a-vm) for more information on the above options. You can also determine supported sizes using the Azure portal, by selecting the VM and under **Settings**, choose **Size**. On the **Size** blade, you can view supported sizes and use filter options.<br>

It should be noted that a VM size being supported in a hardware cluster or region, does not mean that the cluster/region has enough capacity to allocate the VM.<br>

## **Recommended Documents**

- To determine available sizes in the region using Azure CLI see the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command, for the REST API see the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation
- For a conceptual overview on working with VM sizes, availability sets, availability zones, and regions, see [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/)

