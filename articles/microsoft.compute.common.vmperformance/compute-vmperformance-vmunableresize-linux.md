<properties
	pageTitle="Diagnose and resolve Linux Virtual Machine sizing issues"
	description="Diagnose and resolve Linux Virtual Machine sizing issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32690776"
	resourceTags="linux, redhat, Ubuntu"
	productPesIds="16342,15571,15797,16454,16470"
	cloudEnvironments="public, Fairfax"
	articleId="d2152bb1-ed42-4865-bc62-9f391603ea92"
	ownershipId="AzureData_AzureSQLVM"
/>

# Diagnose and resolve Linux Virtual Machine sizing issues

Try the following steps to diagnose and mitigate VM sizing issues.<br>

## **Recommended Steps**

We are experiencing capacity issues for specific regions across the globe. More details can be found by following this link to understand [Our commitment to customers and Microsoft cloud services continuity](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/)<br>

If you are deploying to regions **West Europe, North Europe, UK South, UK West, France Central**, then please be aware that we have an emerging issue related to capacity due to increased usage. In these cases, we recommend trying alternate regions (as first preference) or alternate SKUs.<br>

For general troubleshooting, please follow these steps:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region.<br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))<br>
3. Review troubleshooting documentation for errors you may encounter when resizing a VM in Azure:

    * [Troubleshoot allocation failures when you create, restart, or resize Linux VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/allocation-failure)
    * [Understanding SkuNotAvailable - Some SKU series are unavailable for the selected subscription for this region](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors)<br>
    * [Resolve errors associated with quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors)<br>
    * [Resizing a VM or add VMs to an existing availability set](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure#resize-a-vm-or-add-vms-to-an-existing-availability-set)<br>

4. Review the different VM types in Azure, to resize click 'Size' in the Settings blade of the VM resource:

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
