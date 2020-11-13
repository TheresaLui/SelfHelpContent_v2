<properties
	pageTitle="Diagnose and resolve Linux Virtual Machine Disk performance issues"
	description="Diagnose and resolve Linux Virtual Machine Disk performance issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32640592"
	resourceTags="linux,redhat,ubuntu"
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="compute-virtualdiskmgmt-diskperf-linux"
	ownershipId="Compute_VirtualMachines"
/>

# Diagnose and resolve Linux Virtual Machine Disk performance issues

Azure virtual machines have IOPS and throughput performance limits based on the virtual machine type and size. OS Disks and Data disks, which can be attached to virtual machines, have their own IOPs and throughput limits. When your application running on your virtual machines requests more IOPS or throughput than what is allotted for the virtual machine or the attached disks, your application's performance gets capped. When this happens, the application will experience suboptimal performance and can lead to some negative consequences like increased latency.

## **Recommended Steps**

If you are experiencing issues with disk performance please review our guidance on [Linux Virtual Machines and disk performance](https://docs.microsoft.com/azure/virtual-machines/linux/disk-performance-linux).

**Detection: If you are unaware of the process driving disk consumption, for Linux virtual machines you can  [run PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights-linux).**
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
