<properties
	pageTitle="Diagnose and resolve Linux Virtual Machine Network performance issues"
	description="Diagnose and resolve Linux Virtual Machine Network performance issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32628277"
	resourceTags="linux, redhat, Ubuntu"
	productPesIds="16342,15571,15797,16454,16470"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="b72e0592-b8dc-4d5c-a67d-504d8630b742"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Linux Virtual Machine Network performance issues

Try the following steps to diagnose and mitigate VM Network performance issues.<br>

## **Recommended Steps**

1. **Did you know Performance diagnostics can help you analyze guest VM issues?** **For Linux virtual machines, you can [run Performance diagnostics](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId)** and review results directly from the Azure portal. You may also [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights-linux) and run it on your virtual machine. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
1. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
1. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization.<br>

	* Use commands such as Top, VmStat, Lsof, and Tcpdump.<br>

1. [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth#linux-vm)
1. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)
1. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId) the VM, which migrates it to a new Azure host.<br>

## **Recommended Documents**

* [Azure Virtual Machine Sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes)
* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/linux/compute-benchmark-scores)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [Benchmarking disks in Azure Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/disks-benchmarks#fio)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
* [SQL Server on Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/sql/sql-server-linux-virtual-machines-overview)
