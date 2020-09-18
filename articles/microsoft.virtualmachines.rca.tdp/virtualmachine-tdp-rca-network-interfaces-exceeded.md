<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - Network Interface Account Exceeded"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_rca-networkinterfacecountexceeded"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The operation on virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the number of network interfaces (NICs) requested or attached is greater than the number supported by the VM SKU size.
<!--/issueDescription-->

To avoid this issue, either change the number of network interfaces requested to a value that is supported by the VM SKU. Or, select another SKU that supports that value.<br>

A [**network interface (NIC**](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface) is the interconnection between a VM and a virtual network (VNet). A VM must have at least one NIC, but can have more than one, depending on the size of the VM you create. Learn about how many NICs each VM size supports for [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/sizes) or [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/sizes).<br>

You can create a VM with multiple NICs, and add or remove NICs through the lifecycle of a VM. Multiple NICs allow a VM to connect to different subnets and send or receive traffic over the most appropriate interface. VMs with any number of network interfaces can exist in the same availability set, up to the number supported by the VM size.<br>

Each NIC attached to a VM must exist in the same location and subscription as the VM. Each NIC must be connected to a VNet that exists in the same Azure location and subscription as the NIC. You can change the subnet a VM is connected to after it's created, but you cannot change the VNet. Each NIC attached to a VM is assigned a MAC address that doesn't change until the VM is deleted.<br>

## **Recommended Documents**

* [Overview of network interfaces](https://docs.microsoft.com/azure/virtual-machines/windows/network-overview#network-interfaces)<br>
* [Add network interfaces to or remove network interfaces from virtual machines](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm)<br>
* [More information about VM Sizes - Windows](https://docs.microsoft.com/azure/virtual-machines/windows/sizes)<br>
* [More information about VM Sizes - Linux](https://docs.microsoft.com/azure/virtual-machines/linux/sizes)
