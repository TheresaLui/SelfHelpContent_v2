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
# We need some actions from you to deploy your resource

<!--issueDescription-->
We detected that the deployment for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the availability set **<!--$avsetname-->myAvailabilitySet<!--/$avsetname-->** must be reconfigured to include the VM size specified for the VM that you are resizing.<br>
<!--/issueDescription-->

You attempted to resize a VM to a size that is not available in its current availability set. You can choose a size that is currently available, or resize the VM but to do so you must stop all VMs in the availability set, resize the VM, and then restart the VMs.<br>

You must stop all the VMs so that Azure can configure the availability set to support all the specified VM sizes. To proceed, follow the steps described in [Resize a Windows VM in an availability set](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm#resize-a-windows-vm-in-an-availability-set).

