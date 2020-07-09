<properties
	pageTitle="Diagnose and resolve Virtual Machine performance issues"
	description="Diagnose and resolve Virtual Machine performance issues"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740113"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="fee014a7-7e9b-4758-9f50-329a0fd05ac7"
	ownershipId="AzureData_AzureSQLVM"
/>


# Diagnose and resolve Virtual Machine performance issues

Try the following steps to diagnose and mitigate VM  performance issues.<br>

## **Recommended Steps**

1. **Did you know Performance diagnostics can help you analyze performance on your VM?**<br>
   For Windows virtual machines, you can [run Performance diagnostics](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics), select the Performance analysis scenario, and review results directly from the Azure portal. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. See [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights).<br>
   To ensure a speedy resolution, **provide us the PerfInsights logs** if you create a support case.
2. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
3. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization. On **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon) tool.
4. [Enable monitoring](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running) to identify and remediate issues with Azure VMs and storage
5. Address any Azure host issues by [redeploying](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows) the VM, which migrates it to a new Azure host
6. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource. See [Compute optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-compute)
7. Consider using [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance) if it's an I/O intensive use-case <br>

## **Recommended Documents**

* [Azure Virtual Machine Sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes)
* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/compute-benchmark-scores)
* [SQL Performance guidelines for Azure VMs](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [Benchmarking disks in Azure Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/disks-benchmarks)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
