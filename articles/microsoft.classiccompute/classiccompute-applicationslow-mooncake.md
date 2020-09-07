<properties 
	pageTitle="My application is slow"
	description="My application is slow"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	ms.author="juluk"
	displayOrder="33"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="classiccompute-applicationslow-mooncake"
	ownershipId="Compute_VirtualMachines"
/>

# My application is slow

## **Recommended Steps**

* Keep the external dependencies (Azure SQL, Azure Redis Cache, etc.) that the application accesses in the same region. If the application has numerous external resources, network delays may cause slow performance.
* Review operating system level metrics such as CPU, memory usage, IO, and network. If any resource has consistently high utilization, your application may need more resources than the current hardware provides. Scale out or up if you see resource constraints.
* Review your application's error logs, traces, and metrics. Logs, trace, and metrics can determine if there are any application bottlenecks causing performance issues. A quick way to recover from a one-time issue is to restart your application and machine.
* For further diagnostics, use **DebugDiag**, **ProcDump**, or **WinDbg**. These programs capture memory dumps and give pointers to where the problem might be in the application.

## **Recommended Documents**

* [Troubleshoot using analysis tool to isolate CPU- and memory-related issues](https://channel9.msdn.com/Series/PerfView-Tutorial)
* [Use Perfview to collect and analyze data for performance bottlenecks](http://www.microsoft.com/download/details.aspx?id=28567)
* [Use Debug Diagnostics to troubleshoot a process that has stopped responding](https://support.microsoft.com/kb/919792)
