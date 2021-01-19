<properties
	pageTitle="Received an Allocation Failure"
	description="Received an Allocation Failure"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32743099,32743100,32743101,32743102,32743103"
	resourceTags=""
	productPesIds="14749,15571,15797,16454,16470"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="2e748f25-8996-44f9-8a98-6e1b02b82244"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Received an Allocation Failure

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
