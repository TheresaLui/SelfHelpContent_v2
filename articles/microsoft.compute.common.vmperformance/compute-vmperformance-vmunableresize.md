<properties
	pageTitle="Diagnose and resolve Virtual Machine sizing issues"
	description="Diagnose and resolve Virtual Machine sizing issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32690776"
	resourceTags="windows, windowsSQL"
	productPesIds="14749,14745"
	cloudEnvironments="public, Fairfax"
	articleId="e7920c6e-0eec-4a8f-876d-280f5d4d1035"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Virtual Machine sizing issues

Try the following steps to diagnose and mitigate VM sizing issues.<br>

## **Recommended Steps**

## **Recommended steps**

We are experiencing capacity issues for specific regions across the globe. More details can be found by following this link to understand [Our commitment to customers and Microsoft cloud services continuity](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/)<br>

If you are deploying to regions **West Europe, North Europe, UK South, UK West, France Central**, then please be aware that we have an emerging issue related to capacity due to increased usage. In these cases, we recommend trying alternate regions (as first preference) or alternate SKUs.<br>

For general troubleshooting, please follow these steps:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region.<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))<br>
4. Review troubleshooting documentation for errors you may encounter when resizing a VM in Azure:

    * [Troubleshoot allocation failures when you create, restart, or resize Windows VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/allocation-failure)<br>
    * [Understanding SkuNotAvailable - Some SKU series are unavailable for the selected subscription for this region](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors)<br>
    * [Resolve errors associated with quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors)<br>
    * [Resizing a VM or add VMs to an existing availability set](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure#resize-a-vm-or-add-vms-to-an-existing-availability-set)<br>

5. Review the different VM types in Azure, to resize click 'Size' in the Settings blade of the VM resource:

    * [Azure Virtual Machine Sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes)<br>
    * [General purpose VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-general)<br>
    * [Compute optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-compute)<br>
    * [Memory optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-memory)<br>
    * [Storage optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-storage)<br>
    * [GPU VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-gpu)<br>
    * [High performance compute VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-hpc)

## **Recommended Documents**

* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/compute-benchmark-scores)<br>
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)<br>
* [SQL Performance guidelines for Azure VMs](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)<br>
* [Benchmarking disks in Azure Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/disks-benchmarks)<br>
* [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance)<br>
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
