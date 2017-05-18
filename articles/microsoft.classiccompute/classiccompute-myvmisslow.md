<properties 
	pageTitle="My VM is slow"
	description="My VM is slow "
	service="microsoft.classiccompute"
	resource="virtualmachines"
	authors="kasparks"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds="32411877"
	resourceTags="windows, linux, windowsSQL, redhat"	
	productPesIds="14749"
	cloudEnvironments="public" 
/>
    
# My VM is slow

## **Recommended steps**
Try the following steps to diagnose and mitigate VM performance issues

2. Review your application error logs, traces, and metrics to determine if there are any application bottlenecks causing performance issues. As a quick way to recover from one-time issues, restart your application and machine.
3. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization. <br>
On Windows, use the Perfmon tool. On Linux, use commands such as Top, VmStat, Lsof, and Tcpdump.
4. Use VM Diagnostics and Storage Diagnostics in the Azure portal to identify if any resource is being overutilized or throttled. <br>
[Enable diagnostics, monitor, identify and remediate issues with Azure VMs and Storage](http://aka.ms/azurevmperf)
5. Restart the VM to address any VM operating system issues by clicking 'Restart' at the top of the VM resource blade
6. Scale up the virtual machine to a different VM type or series for increaed performance by clicking 'Size' in the Settings blade of the VM resource
7. Consider using Premium Storage account if its an I/O intensive use-case <br>
[Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/)

## **Recommended documents**
[Detailed troubleshooting of Azure Storage](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/)
