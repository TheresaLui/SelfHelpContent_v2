<properties
	pageTitle="Diagnose and resolve Linux Virtual Machine sizing issues"
	description="Diagnose and resolve Linux Virtual Machine sizing issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32628270"
	resourceTags="linux, redhat, Ubuntu"
	productPesIds="16342,15571,15797,16454,16470"
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="59d5ee22-322d-4b0e-9d2b-fe07bdc1442f"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Linux Virtual Machine sizing issues

## **Recommended Steps**

For general troubleshooting, please follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))<br>
4. Review the different VM types in Azure. To resize, click 'Size' in the Settings blade of the VM resource.

    * [Azure Virtual Machine Sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes)
    * [General purpose VM sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-general)
    * [Compute optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-compute)
    * [Memory optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-memory)
    * [Storage optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-storage)
    * [GPU VM sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-gpu)
    * [High performance compute VM sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-hpc)

## **Recommended Documents**

* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/linux/compute-benchmark-scores)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [Benchmarking disks in Azure Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/disks-benchmarks#fio)
* [Azure Premium Storage: design for high performance](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage-performance)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
* [SQL Server on Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/sql/sql-server-linux-virtual-machines-overview)
