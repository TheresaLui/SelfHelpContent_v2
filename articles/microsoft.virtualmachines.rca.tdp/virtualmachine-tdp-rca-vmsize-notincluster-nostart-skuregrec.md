<properties
	pageTitle="Deployment Failure RCA SkuRegRec"
	description="RCA - VM size not in availability set SkuRegRec"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="OperationFailure_RCA-VMSizeValidation-NotInCluster-Start-SkuRegRec"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your resource and found an issue

The Azure Availability Set chosen in the deployment did not have the needed capacity to allocate the VM. The availability set that this virtual machine was associated with does not support the VM's current size. The VM or availability set must be resized for the start operation to succeed.<br>

>We are currently experiencing high demand for specific regions across the globe. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://aka.ms/CloudCovidResponseFAQ).<br>

We apologize for the inconvenience.<br>

<!--issueDescription-->
We detected that the start operation for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the availability set **<!--$avsetname--> <!--/$avsetname-->** does not support the new SKU Size that you requested.<br>

**<!--$SkuRegRec-->No information provided<!--/$SkuRegRec-->**<br>
<!--/issueDescription-->

An Azure Availability Set is created on a specific hardware cluster based upon the first VM using it. Each subsequent VM added must be compatible with the VM sizes supported in that hardware cluster. By having this constraint, high availability is maintained. In this case, the requested resize size is not available in its current availability set.<br>

## **Recommended Steps**

There are a couple of options depending on your flexibility with SKU options for the availability set:

* Review and use one of the suggested sizes and region pairs provided in the table above.<br>
* Choose a size that is included in your availability set<br>
* Choose a size that is not included in your availability set.<br>

	*However, you must first deallocate all the VMs in the availability set. This is because Azure must deallocate all the VMs in the availability set to reconfigure it to support the new size.*

For PowerShell examples to determine VM sizes in availability sets and to resize a VM, see [Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm).<br>

See [Resize virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines/) for considerations on working with VM sizes, availability sets, regions, and hardware.

## **Recommended Documents**

- [Tutorial: Create and deploy highly available virtual machines with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)
- [Manage the availability of Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)
- [Manage the availability of Linux virtual machines](https://docs.microsoft.com/azure/virtual-machines/linux/manage-availability)
- [Azure Availability Zones](https://azure.microsoft.com/global-infrastructure/availability-zones/)
