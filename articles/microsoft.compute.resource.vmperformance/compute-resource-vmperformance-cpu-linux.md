<properties
	pageTitle="Diagnose and resolve Linux Virtual Machine CPU performance issues"
	description="Diagnose and resolve Linux Virtual Machine CPU performance issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32628261"
	resourceTags="linux, redhat, Ubuntu"
	productPesIds="16342,15571,15797,16454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="9f6417ef-5d01-4c46-8c46-fc5ad86e3869"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Linux Virtual Machine CPU performance issues

**What can cause CPU spike on a VM?**

High CPU can indicate that the application is performing many CPU-intensive tasks relative to the incoming load. This can be an indication that a component used by this application uses is unable to process data as efficiently as expected, that there might be a code issue , or that there are insufficient resources to handle the load that the application is handling. Here are some common factors leading to high CPU:  

1. A recent code change or deployment. This is mostly applicable to apps like Apache, SQL or other applications.
1. A recent patch, which could be related to an OS level patch, or Application level cumulative patches/fixes
1. Query change or outdated Indexes: SQL or Oracle data tier application also have query plan optimization as another factor. Lack of proper indexes, Data changes etc. sometimes lead to some queries getting more compute intensive. 
1. Azure VM Specific: there are certain processes like waagent, extension specific processes (Monitoring Agent, MMA agent, Security client, etc.) which sometimes lead to High CPU consumption and needs to be looked from configuration or known issues perspective

Try the following steps to diagnose and mitigate VM CPU performance issues.

## **Recommended Steps**

**Detection: If you are unaware of the process driving high CPU consumption, you can [access PerfInsights here](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId)** and review results directly from the Azure portal. PerfInsights generates a report that contains a dedicated tab for CPU analysis.  It will list out the processes per Average CPU consumption in descending order. It will point out if the process was a system or application. We have a dedicated Sub-Tab under CPU which could be leveraged for detailed pattern analysis, per core, or per process.

You may also [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics#install-and-run-performance-diagnostics-on-your-vm) and run it in your virtual machine.  

There are two broad approaches to resolving high CPU issues depending upon whether the CPU usage is appropriate given the application load or because of a bug within the application:

1.	If it's expected due to the kind of data or user pattern, then it is recommended to resize to a higher VM SKU**. You can read more about different [Azure Virtual Machine offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/) and decide on which Virtual Machine offering best suits your workload. 
1.	If high CPU is caused due to an application issue, then improving the efficiency of the current application by analyzing the code for potential improvements can help resolve the issue. If the identified application is a third-party application, then you would need to engage the vendor/developer of the application. 

If you are unable to access your virtual machine via RDP or SSH you can try restarting to temporarily regain access, then proceed to troubleshoot using [PerfInsights](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId) to determine what is causing the CPU spike.

**If you proceed to open a support case please attach the PerfInsights report for the Support Engineer to analyze.**

## **Recommended Documents**

* [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
* [Azure Virtual Machine offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/)
* [SQL Server on Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/sql/sql-server-linux-virtual-machines-overview)
* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/linux/compute-benchmark-scores)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [Benchmarking disks in Azure Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/disks-benchmarks#fio)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
