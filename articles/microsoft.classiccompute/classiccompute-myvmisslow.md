<properties
	pageTitle="My VM is slow"
	description="My VM is slow "
	service="microsoft.classiccompute"
	resource="virtualmachines"
	authors="ScottAzure"
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

*As a quick way to recover from one-time issues, restart your application and machine.*<br>

1. **Do you know PerfInsights can help you analyze Guest VM issues?**

	Start here: [Download PerfInsights](https://www.microsoft.com/en-us/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True).<br>

	*To ensure a speedy resolution, you can also provide us the PerfInsights logs if you create a support case.*<br>

2. Review your application error logs, traces, and metrics to determine if there are any application bottlenecks causing performance issues.

3. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization.<br>

	On **Windows**, use the Perfmon tool.<br>
	On **Linux**, use commands such as Top, VmStat, Lsof, and Tcpdump.<br>

4. Use VM Diagnostics and Storage Diagnostics in the Azure portal to identify if any resource is being overutilized or throttled.<br>

	[Enable diagnostics, monitor, identify and remediate issues with Azure VMs and Storage](http://aka.ms/azurevmperf)<br>

5. Restart the VM to address any VM operating system issues by clicking 'Restart' at the top of the VM resource blade.<br>
6. Scale up the virtual machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource.<br>
7. Consider using [Premium Storage for Azure Virtual Machine Workloads](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/).<br>

## **Recommended documents**

* [Detailed troubleshooting of Azure Storage](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/)
