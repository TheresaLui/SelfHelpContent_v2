<properties
	pageTitle="Diagnose and resolve Virtual Machine sizing issues"
	description="Diagnose and resolve Virtual Machine sizing issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32628270"
	resourceTags="windows, windowsSQL"
	productPesIds="14749,14745"
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="b3157bac-dc37-4341-98c8-14320fad6c37"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Virtual Machine sizing issues

## **Recommended Steps**

For general troubleshooting, please follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))<br>
4. Review the different VM types in Azure. To resize, click 'Size' in the Settings blade of the VM resource

    * [Azure Virtual Machine Sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes)
    * [General purpose VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-general)
    * [Compute optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-compute)
    * [Memory optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-memory)
    * [Storage optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-storage)
    * [GPU VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-gpu)
    * [High performance compute VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-hpc)

## **Recommended Documents**

* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/compute-benchmark-scores)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [SQL Performance guidelines for Azure VMs](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)
* [Benchmarking disks in Azure Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/disks-benchmarks)
* [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
