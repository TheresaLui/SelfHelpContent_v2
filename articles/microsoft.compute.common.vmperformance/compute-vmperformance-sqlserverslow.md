<properties
	pageTitle="Diagnose and resolve performance issues with SQL Server in a VM"
	description="Diagnose and resolve performance issues with SQL Server in a VM"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32742813"
	resourceTags="windows, windowsSQL"
	productPesIds="14749"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="compute-vmperformance-sqlserverslow"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve performance issues with SQL Server in a VM

Try the following steps to diagnose and mitigate VM CPU performance issues.<br>

## **Recommended Steps**

1. For SQL Server on Azure VM, we **strongly recommend** that you follow the [Performance Guidelines for SQL Server on Azure VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance).

1. We recommend that you use the same database performance [tuning options](https://docs.microsoft.com/archive/msdn-magazine/2008/january/sql-server-uncover-hidden-data-to-optimize-application-performance) that are applicable to SQL Server in any SQL server environment: 
    1. Consider adding [missing indexes](https://gallery.technet.microsoft.com/Find-statements-for-13e8c2f4) which can help improve query performance
    1. Consider [updating statistics](https://docs.microsoft.com/sql/relational-databases/maintenance-plans/update-statistics-task-maintenance-plan?view=sql-server-ver15) if possible with Full Scan and for all tables of the database(s) of interest
1. **Did you know Performance diagnostics can help you analyze performance on your VM?** **For Windows virtual machines, you can [run Performance diagnostics](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics)**, and review results directly in the Azure portal. 
    1. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. 
    1. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
1. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
1. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization. On **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon) tool.
1. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)<br>
1. Address any Azure host issues by [redeploying](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows) the VM, which migrates it to a new Azure host
1. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource.  [Compute optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-compute)
1. Consider using [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance) if it's an I/O intensive use-case <br>

## **Recommended Documents**

* [Performance best practices for SQL VM](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance/)<br>
* [Storage configuration guidelines for SQL VM](https://blogs.msdn.microsoft.com/sqlserverstorageengine/2018/09/25/storage-configuration-guidelines-for-sql-server-on-azure-vm/)
* [OS best practice configurations for SQL Server](https://blogs.msdn.microsoft.com/docast/2018/02/01/operating-system-best-practice-configurations-for-sql-server/)
* [Azure VM Storage performance](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices#storage-guidance)
* [Designing for high performance](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance)
* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/compute-benchmark-scores)
* [Benchmarking disks in Azure Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/disks-benchmarks)
