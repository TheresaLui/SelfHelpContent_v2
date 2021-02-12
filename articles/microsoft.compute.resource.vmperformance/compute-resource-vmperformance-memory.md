<properties
	pageTitle="Diagnose and resolve Virtual Machine Memory performance issues"
	description="Diagnose and resolve Virtual Machine Memory performance issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32628275"
	resourceTags="windows, windowsSQL"
	productPesIds="14749,14745"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="e745bc24-2714-4ba7-993f-9491e93a538a"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Virtual Machine Memory performance issues

**What can cause Memory Pressure on a VM?**

* The load pattern is Memory intensive, in which case the consistent/intermittent Memory Pressure is expected
* Was there a recent code change which might be causing memory leak?
* Was there a recent change in number of users or spike in amount of data processing?
* Does it correlate with a job processing e.g. maintenance, indexing, cube processing, end of day reporting?
* A system process after a recent OS patch, could be causing memory leak?

## **Recommended Steps**

**Detection: If we are unaware of the process causing high Memory Pressure, you can [access PerfInsights here](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId)** and review results directly from the Azure portal. You may also [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics#install-and-run-performance-diagnostics-on-your-vm) and run it in your virtual machine. PerfInsights generates a report that has a dedicated tab for Memory analysis.

If you are unable to access your virtual machine via RDP or SSH you can try restarting to temporarily regain access, then proceed to troubleshoot using [PerfInsights](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId) to determine what is causing the memory pressure.

**If it is expected due to the kind of data or user pattern, then it is recommended to resize to higher VM SKU**. You can read about different [Azure Virtual Machine offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/) and decide on which Virtual Machine offering best suits your workload.


## **Recommended Documents**

* [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
* [Azure Virtual Machine offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/)
* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/compute-benchmark-scores)
* [SQL Performance guidelines for Azure VMs](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [Benchmarking disks in Azure Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/disks-benchmarks)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
