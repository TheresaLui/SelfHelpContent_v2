<properties
	pageTitle="performance/slow virtual machine"
	description="performance/slow virtual machine"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure,timbasham"
	ms.author="scotro,tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32511162,32628264,32628261,32628277,32628254,32628275,32628268,32628281,32628270"
	resourceTags=""
	productPesIds="14749,14745"
	cloudEnvironments="public"
	articleId="9acfc4d8-fdbf-4381-b9bc-aff0a19de511"
/>

# My VM is slow

4 out of 5 customers resolved their performance issue using the below steps.<br>

## **Recommended Steps**

1. **Did you know Performance diagnostics can help you analyze guest VM issues?** **For Windows virtual machines, you can [run Performance diagnostics](https://docs.microsoft.com/azure/virtual-machines/windows/how-to-use-perfinsights)** and review results directly from the Azure portal. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [Learn more](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics)
2. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
3. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization. On **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon) tool.
4. Use VM Diagnostics and Storage Diagnostics in the Azure portal to identify if any resource is being overutilized or throttled <br>
5. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)<br>
6. Address any Azure host issues by [redeploying](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows#use-the-azure-portal) the VM, which migrates it to a new Azure host
7. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource
8. Consider using [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage) if it's an I/O intensive use-case <br>

## **Recommended documents**

* [How to use the self-help diagnostic tool - PerfInsights](https://docs.microsoft.com/azure/virtual-machines/windows/how-to-use-perfinsights)<br>
* [Performance diagnostics for Azure virtual machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics)<br>
* [Troubleshoot common performance root cause - Storage IO](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
* [Azure Performance Diagnostics VM Extension for Windows](https://docs.microsoft.com/azure/virtual-machines/windows/performance-diagnostics-vm-extension)<br>
* [Azure Premium Storage: Design for High Performance](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance)<br>
* [Configure VMs for optimal Storage performance](https://blogs.msdn.microsoft.com/mast/2014/10/14/configuring-azure-virtual-machines-for-optimal-storage-performance/)<br>
* [Performance guidelines for SQL Server in Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)
