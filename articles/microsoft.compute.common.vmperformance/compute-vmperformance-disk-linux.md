<properties
	pageTitle="Diagnose and resolve Linux Virtual Machine Storage performance issues"
	description="Diagnose and resolve Linux Virtual Machine Storage performance issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32628264"
	resourceTags="linux, redhat, Ubuntu"
	productPesIds="16342,15571,15797,16454,16470"
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="e32c32c4-edf2-470f-a731-7f4fe2cff95d"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Linux Virtual Machine Storage performance issues

Try the following steps to diagnose and mitigate VM Storage performance issues.<br>

## **Recommended Steps**

1. **Did you know Performance diagnostics can help you analyze performance on your VM?** **For Linux virtual machines, you can [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights-linux) and run it on your virtual machine.** To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [Learn more](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics)
2. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
3. Using commands such as Top, VmStat, Lsof, and Tcpdump, review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization
4. Use [FIO](https://docs.microsoft.com/azure/virtual-machines/linux/disks-benchmarks#fio) to benchmark your VM disk performance
5. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)<br>
6. Address any Azure host issues by [redeploying](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-linux) the VM, which migrates it to a new Azure host
7. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource. [Storage optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-storage)<br>
8. Consider using [Azure Premium Storage: design for high performance](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage-performance) if its an I/O intensive use-case <br>


## **Recommended Documents**

* [Azure Virtual Machine Sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes)
* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/linux/compute-benchmark-scores)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [Benchmarking disks in Azure Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/disks-benchmarks#fio)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
* [SQL Server on Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/sql/sql-server-linux-virtual-machines-overview)
