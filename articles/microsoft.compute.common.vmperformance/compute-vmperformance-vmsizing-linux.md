<properties
	pageTitle="Diagnose and resolve Linux Virtual Machine sizing issues"
	description="Diagnose and resolve Linux Virtual Machine sizing issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32628264,32628261,32628277,32628254,32628275,32628268,32628281,32628270"
	resourceTags="linux, redhat, Ubuntu"
	productPesIds="16342,15571,15797,16454"
	cloudEnvironments="public"
	articleId="55e5b484-ddbe-497f-bd1d-9adcb30216f8"
/>

# Diagnose and resolve Linux Virtual Machine sizing issues

Try the following steps to diagnose and mitigate VM sizing issues.<br>

## **Recommended Steps**

1. **Did you know Performance diagnostics can help you analyze performance on your VM?** **For Linux virtual machines, you can [download PerfInsights](https://aka.ms/perfinsightslinux) and run it on your virtual machine.** To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [Learn more](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics)
2. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization.<br>

	* Use commands such as Top, VmStat, Lsof, and Tcpdump.<br>

3. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)<br>
4. Review the different VM types in Azure, to resize click 'Size' in the Settings blade of the VM resource. 
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
