<properties
  pagetitle="Diagnose and resolve Linux Virtual Machine Storage performance issues"
  service="microsoft.compute"
  resource="virtualmachines"
  ms.author="tibasham,babhoo"
  selfhelptype="Generic"
  supporttopicids="32628264"
  resourcetags="linux,redhat,ubuntu"
  productpesids="15571,15797,16454,16470,14749"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="e32c32c4-edf2-470f-a731-7f4fe2cff95d"
  ownershipid="Compute_VirtualMachines_Content" />
# Diagnose and resolve Linux Virtual Machine Storage performance issues

To diagnose and mitigate virtual machine (VM) storage performance issues, try the following steps and review the following documents.

## **Recommended Steps**

1. **Performance diagnostics can help you analyze performance on your VM. For Linux virtual machines, you can download [PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights-linux) and run it on your virtual machine.** For more information, see [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights). 
You can also download [PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics#install-and-run-performance-diagnostics-on-your-vm) and run it on your VM.  
*If you proceed to open a support case, attach the PerfInsights report for the Support Engineer to analyze.*
2. Review your application error logs, traces, and metrics to determine if any application-level bottlenecks are causing performance issues. To quickly recover from one-time issues, restart your application and VM.
3. Use commands such as `Top`, `VmStat`, `Lsof`, and `Tcpdump`, and review operating system level metrics such as CPU, memory usage, IO, and network, to see if any resource has consistently high usage
4. Use [FIO](https://docs.microsoft.com/azure/virtual-machines/linux/disks-benchmarks#fio) to benchmark your VM disk performance
5. Enable [diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)
6. Address any Azure host issues by [redeploying](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-linux) the VM, which migrates it to a new Azure host
7. Scale up the VM to a different VM type or series for increased performance by clicking **Size** in the **Settings** blade of the VM resource. For more information, see [Storage optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-storage).
8. If it's an intensive I/O use case, consider using [Azure Premium Storage: design for high performance](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage-performance)
9. Consider using Premium SSDs for [ flexibility to increase disk performance without increasing the actual disk size](https://docs.microsoft.com/azure/virtual-machines/disks-performance-tiers)

## **Recommended Documents**

* [Azure Virtual Machine Sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes)
* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/linux/compute-benchmark-scores)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [Benchmarking disks in Azure Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/disks-benchmarks#fio)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
* [SQL Server on Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/sql/sql-server-linux-virtual-machines-overview)
