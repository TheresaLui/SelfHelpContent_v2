<properties
	pageTitle="Diagnose and resolve Virtual Machine sizing issues"
	description="Diagnose and resolve Virtual Machine sizing issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32628270"
	resourceTags="windows, windowsSQL"
	productPesIds="14749,14745"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="944d5b78-5b69-4c12-b65c-0eec1681ec6c"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Virtual Machine sizing issues

Try the following steps to diagnose and mitigate VM sizing issues.<br>

## **Recommended Steps**

1. **Did you know Performance diagnostics can help you analyze performance on your VM?** **For Windows virtual machines, you can [run Performance diagnostics](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId)** select the Performance analysis scenario, and review results directly from the Azure portal. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
2. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization. On **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon) tool.
3. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)<br>
4. Review the different VM types in Azure, to resize click 'Size' in the Settings blade of the VM resource.  
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
