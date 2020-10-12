<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - Existing-avset-was-not-deployed-on-acceleratednetworkingenabledcluster"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-existing-avset-was-not-deployed-on-acceleratednetworkingenabledcluster"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed for the following reason: enabling the availability set for accelerated networking is not possible as the cluster does not support that functionality..
<!--/issueDescription-->

When enabling Accelerated Networking for an availability set, the *availability set* must be deployed on an ***Accelerated Networking enabled cluster***. If you are creating a VM with *Accelerated Networking* and encounter this issue, all VMs in an availability set or VMSS must be stopped/deallocated before enabling Accelerated Networking on any NIC. For additional information, refer to [Enable Accelerated Networking on existing VMs using CLI](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli#enable-accelerated-networking-on-existing-vms) and [PowerShell](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)<br>

To learn more about Accelerated Networking, please refer to the following articles:<br>

* [Create a virtual machine with Accelerated Networking](https://docs.microsoft.com/azure/virtual-network/virtual-network-create-vm-accelerated-networking)<br>
* [Limitations with creating virtual machines with Accelerated Networking](https://docs.microsoft.com/azure/virtual-network/virtual-network-create-vm-accelerated-networking#Limitations)
