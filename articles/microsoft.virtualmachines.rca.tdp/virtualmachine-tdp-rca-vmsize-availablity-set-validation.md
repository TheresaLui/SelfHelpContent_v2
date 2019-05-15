<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - VM size not in availability set"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-VMSizeValidation_NotInCluster_NewVM"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue 

<!--issueDescription-->
We detected that the operation **<!--$OperationName-->operationName<!--/$OperationName-->** on virtual machine **<!--$vmname-->myVirtualMachine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the requested VM size is not available in the current hardware cluster where the Azure Availability Set **<!--$avsetname-->myAvailabiltySet<!--/$avsetname-->** is created.<br>
<!--/issueDescription-->

An Azure Availability Set is created based upon the first VM applied to it and operates using a specific hardware cluster as determined by the Azure fabric. Each subsequent VM added to the availability set must be compatible with the VM sizes supported in the hardware cluster. By having this constraint, high availability is maintained.

We apologize for any inconvenience in not being able to use your desired VM size, but have a couple of options depending on your flexibility with SKU options for the availability set:

•	If you not limited to a specific SKU, you can query the available VM sizes for your current availability set and pick a suitable size from the results by using the PowerShell `Get-AzVMSize` command and its parameters. See [Check for available VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets#check-for-available-vm-sizes) where you can run the command directly. 

•	If you are limited to a specific SKU, you must create a new availability set based on the VM that matches your required SKU. Afterwards, you may need to deallocate the existing availability set.

## Resources

| To learn about ... | See these articles |
| --- | --- |
| Availability sets | [Tutorial: Create and deploy highly available virtual machines with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) |
| Manage availability sets for Windows VMs | [Manage the availability of Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability) |
| Manage availability sets for Linux VMs | [Manage the availability of Linux virtual machines](https://docs.microsoft.com/azure/virtual-machines/linux/manage-availability) |
