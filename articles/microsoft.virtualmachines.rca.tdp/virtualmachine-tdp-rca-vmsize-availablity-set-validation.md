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
We detected that a failure for the **<!--$OperationName-->operation<!--/$OperationName-->** on virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because it has an invalid size for the in the **<!--$avsetname-->Availability set name<!--/$avsetname-->** availability set.<br>
<!--/issueDescription-->

Availability sets are configured to support only specified VM sizes according to the hardware capabilities of the cluster of underlying hosts that service the availability set. To add a VM to availbilty set, it must match one of the specified VM sizes.

To determine supported VM sizes for a availability set, see [Check for available VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets#check-for-available-vm-sizes). This is one of the procedures desribed in the [Tutorial: Create and deploy highly available virtual machines with Azure PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets#check-for-available-vm-sizes).

If you need to resize a VM to include in an availability set, you must deallocate all VMs in that availability set to resize the VM that you want to include. For examples in PowerShell, wee [Resize a Windows VM in an availability set](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm#resize-a-windows-vm-in-an-availability-set). 





