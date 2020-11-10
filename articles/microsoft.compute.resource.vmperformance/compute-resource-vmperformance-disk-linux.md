<properties
	pageTitle="Diagnose and resolve Linux Virtual Machine Disk performance issues"
	description="Diagnose and resolve Linux Virtual Machine Disk performance issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32628264"
	resourceTags="linux, redhat, Ubuntu"
	productPesIds="16342,15571,15797,16454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="165e9160-a06b-4279-873b-5faa1cefbcba"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Linux Virtual Machine Disk performance issues

Azure virtual machines have IOPS and throughput performance limits based on the virtual machine type and size. OS Disks and Data disks, which can be attached to virtual machines, have their own IOPs and throughput limits. When your application running on your virtual machines requests more IOPS or throughput than what is allotted for the virtual machine or the attached disks, your application's performance gets capped. When this happens, the application will experience suboptimal performance and can lead to some negative consequences like increased latency.

## **Recommended Steps**

**Detection: If you are unaware of the process driving disk consumption, you can [access PerfInsights here](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId)** and review results directly from the Azure portal. PerfInsights generates a report that contains a dedicated tab for storage analysis.

You may also [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics#install-and-run-performance-diagnostics-on-your-vm) and run it in your virtual machine.   

*If you proceed to open a support case, attach the PerfInsights report for the Support Engineer to analyze.*

### Additional tools and guidance for troubleshooting disk performance

1. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-performance-virtual-machine-linux-windows)
1. Review your application error logs, traces, and metrics to determine if any application-level bottlenecks are causing performance issues. To quickly recover from one-time issues, restart your application and VM.
1. Review operating system level metrics such as CPU, memory usage, I/O, and network to see if any resource has consistently high utilization. Use commands such as `Top`, `VmStat`, `Lsof`, `iostat`, and `Tcpdump`.
1. Use [FIO](https://docs.microsoft.com/azure/virtual-machines/linux/disks-benchmarks#fio) to benchmark your VM disk performance
1. Address any Azure host issues by [redeploying](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-linux) the VM, which migrates it to a new Azure host.
1. Scale up the VM to a different VM type or series for increased performance by clicking **Size** in the **Settings** blade of the VM. For more information, see [Storage optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-storage).
1. If your workload is I/O intensive, consider using [Azure Premium Storage: design for high performance](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage-performance)
1. Consider using Premium SSDs for [flexibility to increase disk performance without increasing the actual disk size](https://docs.microsoft.com/azure/virtual-machines/disks-performance-tiers?toc=/azure/virtual-machines/linux/toc.json)


## **Recommended Documents**

* [Linux Virtual Machine and disk performance](https://docs.microsoft.com/azure/virtual-machines/linux/disk-performance-linux)
* [Optimize Linux Virtual Machine performance](https://docs.microsoft.com/azure/virtual-machines/linux/optimization)
* [Benchmarking disks in Azure Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/disks-benchmarks#fio)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
* [Azure Virtual Machine Sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes)
* [Azure Compute benchmark scores for Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/compute-benchmark-scores)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [SQL Server on Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/sql/sql-server-linux-virtual-machines-overview)
