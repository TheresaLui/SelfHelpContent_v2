<properties
	pageTitle="Deployment Failure RCA SkuRegRec"
	description="RCA - VM size not in availability set SkuRegRec"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-VMSizeValidation_NotInCluster_NewVM-SkuRegRec"
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
We detected that the operation **<!--$OperationName-->operationName<!--/$OperationName-->** on virtual machine **<!--$vmname-->myVirtualMachine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the requested VM size is not available in the current hardware cluster where the Azure Availability Set **<!--$avsetname-->myAvailabilitySet<!--/$avsetname-->** is created.<br>

**<!--$SkuRegRec-->No information provided<!--/$SkuRegRec-->**<br>
<!--/issueDescription-->

An Azure Availability Set is created on a specific hardware cluster based upon the first VM using it. Each subsequent VM added must be compatible with the VM sizes supported in that hardware cluster. By having this constraint, high availability is maintained.<br>

There are a couple of options depending on your flexibility with SKU options for the availability set:

* Review and use one of the suggested sizes and region pairs provided in the table above.<br>
* If you are not limited to a specific SKU, you can query the available VM sizes for your current availability set and pick a suitable size from the results by using the PowerShell [Get-AzVMSize](https://docs.microsoft.com/powershell/module/az.compute/get-azvmsize) command. See [Check for available VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets#check-for-available-vm-sizes) where you can run the command directly.<br>
* If you are limited to a specific SKU, you must create a new availability set based on the VM that matches your required SKU. Afterwards, you may need to deallocate the existing availability set.

In addition, you can consider Azure Availability Zones which provides high availability by having VMs grouped in one or more physical locations within an Azure Region.<br>

## **Recommended Documents**

| To learn about ... | See these articles |
| --- | --- |
| Availability sets | [Tutorial: Create and deploy highly available virtual machines with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) |
| Manage availability sets for Windows VMs | [Manage the availability of Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability) |
| Manage availability sets for Linux VMs | [Manage the availability of Linux virtual machines](https://docs.microsoft.com/azure/virtual-machines/linux/manage-availability) |
| Availability Zones | [Azure Availability Zones](https://azure.microsoft.com/global-infrastructure/availability-zones/) |
| Availability Sets compared with Availability Zones | [Azure VMs : Availability Sets and Availability Zones](https://social.technet.microsoft.com/wiki/contents/articles/51828.azure-vms-availability-sets-and-availability-zones.aspx) |
