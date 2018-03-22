<properties 
	pageTitle="My VM is slow"
	description="My VM is slow"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="kasparks"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds="32411877"
	resourceTags="windows, linux, windowsSQL, redhat"	 
	productPesIds="14749"
	cloudEnvironments="MoonCake"
/>

# My VM is slow

## **Recommended steps**

Try the following steps to diagnose and mitigate VM performance issues.

1. **Do you know PerfInsights can help you analyze Guest VM issues?** Start here: [Download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True).<br> To ensure a speedy resolution, you can also provide us the PerfInsights logs if you create a support case.
2. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues <br>
As a quick way to recover from one-time issues, restart your application and virtual machine
3. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization <br>
On Windows, use the Perfmon tool. On Linux, use commands such as Top, VmStat, Lsof, and Tcpdump.
4. Use VM Diagnostics and Storage Diagnostics in the Azure portal to identify if any resource is being overutilized or throttled <br>
[Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)
5. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeploy) the VM, which migrates it to a new Azure host.
6. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource
7. Consider using a Premium Storage account if its an I/O intensive use-case <br>
[Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.azure.cn/storage/storage-premium-storage/)

## **Recommended documents**
[Detailed troubleshooting of Azure Storage](https://docs.azure.cn/storage/storage-monitoring-diagnosing-troubleshooting/)
