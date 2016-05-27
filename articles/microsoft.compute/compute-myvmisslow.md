<properties 
	pageTitle="My VM is slow"
	description="My VM is slow"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="kasparks"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="windows, linux"	 
	productPesIds=""
	cloudEnvironments="public"
/>

# My VM is slow

## **Recommended steps**
Try the following steps to diagnose and mitigate VM performance issues.

1. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues <br>
As a quick way to recover from one-time issues, restart your application and virtual machine
2. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization <br>
On Windows, use the Perfmon tool. On Linux, use commands such as Top, VmStat, Lsof, and Tcpdump.
3. Use VM Diagnostics and Storage Diagnostics in the Azure portal to identify if any resource is being overutilized or throttled <br>
[Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](http://aka.ms/azurevmperf)
4. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeploy) the VM, which migrates it to a new Azure host.
5. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource
6. Consider using a Premium Storage account if its an I/O intensive use-case <br>
[Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/)

## **Recommended documents**
[Detailed troubleshooting of Azure Storage](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/)