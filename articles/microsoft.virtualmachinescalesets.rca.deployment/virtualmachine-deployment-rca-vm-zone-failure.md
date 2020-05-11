<properties
	pageTitle="Allocation Failure RCA"
	description="RCA - VM size not in zone"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachinescalesets"
	authors="summertgu"
	ms.author="tiag"
	displayOrder=""
	articleId="VMSS_OperationFailure_RCA-VMSizeValidation-ZoneAllocationFailure"
	diagnosticScenario="OperationFailure"
	selfHelpType="rca"
	supportTopicIds="32641079,32641082,32641076,32641075,32641080,32641074,32641076,32641077,32641072,32641073"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We detected that the deployment for virtual machine scale set **<!--$vmssname-->Virtual machine scale set<!--/$vmssname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the availability zone **<!--$zonenumber--> <!--/$zonenumber-->** does not have the capacity to support its allocation.<br>
<!--/issueDescription-->

The Azure Availability Zone chosen in the deployment did not have the needed capacity to allocate the VM. Availability zones are physically separate locations within an Azure region that provide high availability to protect your applications and data from datacenter failures.<br>  

## **Recommended Steps**

We apologize for the inconvenience. Please try allocating the VM scale set again as the issue might have been temporary and there now could be sufficient resources for the allocation. If that doesn't work, you have the following options:<br>

- Resize the VM instance to a size that is currently available in your region. If you are using an older VM product, consider newer versions.
- Deploy a new VM instance to another availability zone in the region

To determine available sizes in the Azure portal, select the VM and under **Settings**, choose **Size**. On the **Size** blade, you can view available sizes and use filter options.<br>

## **Recommended Documents**

-  To determine sizes using PowerShell, use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command, for Azure CLI see the [az vmss list-skus](https://docs.microsoft.com/cli/azure/vmss?view=azure-cli-latest#az-vmss-list-skus) command, for the REST API see the [Virtual Machine Scale Sets - List Skus](https://docs.microsoft.com/rest/api/compute/virtualmachinescalesets/listskus) and [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operations
- See [Resize a Windows VM not in an availability set](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm#resize-a-windows-vm-not-in-an-availability-set) to resize a VM that's not in an availability set using PowerShell
- See [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/) for a conceptual overview on working with VM sizes, availability sets, availability zones, and regions
