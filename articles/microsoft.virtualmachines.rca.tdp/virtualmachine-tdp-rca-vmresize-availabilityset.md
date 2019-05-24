<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - VM size not in region"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-VMSizeValidation_NotInCluster"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We detected that the update operation for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the availability set **<!--$avsetname--> <!--/$avsetname-->** does not support the new SKU Size that you requested.<br>
<!--/issueDescription-->

An Azure Availability Set is created on a specific hardware cluster based upon the first VM using it. Each subsequent VM added must be compatible with the VM sizes supported in that hardware cluster. By having this constraint, high availability is maintained. In this case, the resize attempt used a size that is not available in its current availability set/hardware cluster.

We apologize for any inconvenience in not being able to use your desired VM size, but have a couple of options depending on your flexibility with SKU options for the availability set:

- Choose a size that is included in your availability set.
- Choose a size that is not included in your availability set. However, you must first deallocate all the VMs in the availability set. This is because Azure must have all the VMs deallocated in the set to reconfigure them to support the new size.<br> 

## Resources

In addition to availability sets, consider Azure Availability Zones. Availability zones provide high availability by having VMs grouped in one or more physical locations within an Azure Region.<br>

| To learn about ... | See these articles |
| --- | --- |
| Availability Zones | [Azure Availability Zones](https://azure.microsoft.com/global-infrastructure/availability-zones/) |
| Availability sets compared with availability zones | [Azure VMs : Availability Sets and Availability Zones](https://social.technet.microsoft.com/wiki/contents/articles/51828.azure-vms-availability-sets-and-availability-zones.aspx) |
| Availability sets | [Tutorial: Create and deploy highly available virtual machines with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) |
| Manage availability sets for Windows VMs | [Manage the availability of Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability) |
| Manage availability sets for Linux VMs | [Manage the availability of Linux virtual machines](https://docs.microsoft.com/azure/virtual-machines/linux/manage-availability) |



