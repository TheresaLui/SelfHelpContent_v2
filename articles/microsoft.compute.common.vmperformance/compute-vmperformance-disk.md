<properties
  pagetitle="Diagnose and resolve Windows Virtual Machine Disk performance issues"
  description="Diagnose and resolve Windows Virtual Machine Disk performance issues"
  service="microsoft.compute"
  resource="virtualmachines"
  authors="timbasham"
  ms.author="tibasham,babhoo"
  displayorder="15"
  selfhelptype="Generic"
  supporttopicids="32628264"
  resourcetags="windows, windowsSQL"
  productpesids="14749,14745"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="1846ef6d-3aa8-44c1-bff0-cc8ede1933c6"
  ownershipid="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Virtual Machine Disk performance issues

Azure virtual machines have IOPS and throughput performance limits based on the virtual machine type and size. OS Disks and Data disks, which can be attached to virtual machines, have their own IOPs and throughput limits. When your application running on your virtual machines requests more IOPS or throughput than what is allotted for the virtual machine or the attached disks, your application's performance gets capped. When this happens, the application will experience suboptimal performance and can lead to some negative consequences like increased latency.

## **Recommended Steps**

If you are experiencing issues with disk performance please review our guidance on [Windows Virtual Machines and disk performance](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows).

**Detection: If you are unaware of the process driving disk consumption, for Windows virtual machines you can [run PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights).**
*If you proceed to open a support case please attach the PerfInsights report for the Support Engineer to analyze.*

### Additional tools and guidance for troubleshooting disk performance

1. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)
1. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
1. Review operating system level metrics such as IO, CPU, memory usage, and network to see if any resource has consistently high utilization. On **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon), and [Iometer](https://docs.microsoft.com/azure/virtual-machines/windows/disks-benchmarks#iometer)
1. Address any Azure host issues by [redeploying](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows) the VM, which migrates it to a new Azure host
1. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking **Size** in the **Settings** blade of the VM. For more information, see [Storage optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-storage)
1. If your workload is I/O intensive, consider using [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance)
1. Consider using Premium SSDs for [flexibility to increase disk performance without increasing the actual disk size](https://docs.microsoft.com/azure/virtual-machines/disks-performance-tiers?toc=/azure/virtual-machines/windows/toc.json)

## **Recommended Documents**

* [Windows Virtual Machines and disk performance](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows)
* [Benchmarking disks in Azure Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/disks-benchmarks)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
* [Azure Virtual Machine Sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes)
* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/compute-benchmark-scores)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [SQL Performance guidelines for Azure VMs](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)
