<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - cannotaddvmwithacceleratednetworkingenablednics"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-cannotaddvmwithacceleratednetworkingenablednics"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed for the following reason: a virtual machine with Accelerated Networking Enabled nics cannot be added to an existing non-accelerated networking Availability Set.
<!--/issueDescription-->

To work around this issue, please deploy the virtual machine into an Availability Set that has accelerated networking already enabled.<br>

To learn more about Accelerated Networking, please refer to the following articles:<br>
* [Create a virtual machine with Accelerated Networking](https://docs.microsoft.com/azure/virtual-network/virtual-network-create-vm-accelerated-networking)<br>
* [Limitations with creating virtual machines with Accelerated Networking](https://docs.microsoft.com/azure/virtual-network/virtual-network-create-vm-accelerated-networking#Limitations)<br>