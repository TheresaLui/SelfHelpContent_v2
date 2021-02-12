<properties
	pageTitle="I received an allocation failure"
	description="I received an allocation failure"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32628252,32628253"
	resourceTags=""
	productPesIds="14749,15571,15797,16454,16470"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="9c0b9ec9-a07a-40e3-a6a2-f4d49f5f4ccb"
	ownershipId="Compute_VirtualMachines_Content"
/>

# I received an allocation failure

## **Recommended Steps**

For general troubleshooting, please follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))<br>
4. Review the different VM types in Azure. To resize, click 'Size' in the Settings blade of the VM resource.

## **Recommended Documents**

* [Restarting a partially stopped (deallocated) VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure#restart-partially-stopped-deallocated-vms)<br>
* [Resizing a VM or add VMs to an existing availability set](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure#resize-a-vm-or-add-vms-to-an-existing-availability-set)<br>
* [Restarting a fully stopped (deallocated) VMs](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure#restart-fully-stopped-deallocated-vms)<br>
* [Allocation failures for older VM sizes (Av1, Dv1, DSv1, D15v2, DS15v2, etc.)](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure#allocation-failures-for-older-vm-sizes-av1-dv1-dsv1-d15v2-ds15v2-etc)<br>
* [Allocation failures for large deployments (more than 500 cores)](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure#allocation-failures-for-large-deployments-more-than-500-cores)
* [Troubleshoot allocation failures when creating a new virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)<br>
* [Classic Deployments: Troubleshoot allocation failures](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure-classic)
