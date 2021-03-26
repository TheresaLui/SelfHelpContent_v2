<properties
	pageTitle="Accelerated Networking"
	description="Accelerated Networking"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32788601"
	resourceTags=""
	productPesIds="14749,15571,15797,16454,16208,16470"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="dda6b0e2-f75d-4617-a4ac-a04d0bc8651ac"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Accelerated Networking

Most customers resolve their Azure Accelerated Networking issue using the following resources.<br>

Accelerated networking enables single root I/O virtualization (SR-IOV) to a VM, greatly improving its networking performance. This high-performance path bypasses the host from the data path, which reduces latency, jitter, and CPU utilization for the most demanding network workloads on supported VM types.<br>

## **Recommended Documents**

* [Overview](https://docs.microsoft.com/azure/architecture/topics/high-performance-computing#introduction-to-hpc)<br>
* [Creating a Windows VM with accelerated netwporking](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell)
* [Creating a Linux VM with accelerated networking](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli)
* [Limitations and constraints](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell#limitations-and-constraints)
* [Enabling accelerated networking on existing VMs](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-powershell#enable-accelerated-networking-on-existing-vms)
