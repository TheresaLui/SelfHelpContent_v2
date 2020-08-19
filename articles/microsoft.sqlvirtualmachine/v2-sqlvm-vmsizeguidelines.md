<properties
	pageTitle="VM size guidelines"
	description="VM size guidelines"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,yareyes,amamun"	
	authors="ujpat,yareyes,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740115"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="241ff2c5-a997-48bc-b9b2-9a1a1d7bcc06"
	ownershipId="AzureData_AzureSQLVM"
/>


# VM size guidelines

## **Recommended Steps**

For general troubleshooting, please follow these guidelines:

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))
2. Deploy to another region
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))
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


## **Recommended Documents related to SQL Configuration**

* [Storage Configuration Guidelines for SQL Server on Azure VM](https://blogs.msdn.microsoft.com/sqlserverstorageengine/2018/09/25/storage-configuration-guidelines-for-sql-server-on-azure-vm/)<br>
* [Storage configuration for SQL Server VMs](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-storage-configuration)

