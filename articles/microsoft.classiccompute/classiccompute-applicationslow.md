<properties 
	pageTitle="My application is slow"
	description="My application is slow"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
	articleId="56941257-e147-4087-b24a-40bb08041e08"
	ownershipId="Compute_AppService"
/>

# My application is slow

## **Recommended steps**
1.	Keep the external dependencies (SQL Azure, Azure Redis Cache, etc.) that the application accesses in the same region. <br>
If the application has numerous external resources, network delays may cause slow performance.
2.	Review operating system level metrics such as CPU, memory usage, IO, and network. <br>
If any resource has consistently high utilization, your application may need more resources than the current hardware provides. Scale out or up if you see resource constraints. 
3.	Review your application's error logs, traces, and metrics. <br>
Logs, trace, and metrics can determine if there are any application bottlenecks causing performance issues. A quick way to recover from a one-time issue is to restart your application and machine.
4.	For further diagnostics, use [DebugDiag] (https://msdn.microsoft.com/library/ff420662.aspx), **ProcDump**, or **WinDbg**. <br> 
These programs capture memory dumps and give pointers to where the problem might be in the application.

## **Recommended documents**
[Troubleshoot using analysis tool to isolate CPU- and memory-related issues](https://channel9.msdn.com/Series/PerfView-Tutorial)<br>
[Use Perfview to collect and analyze data for performance bottlenecks](http://www.microsoft.com/download/details.aspx?id=28567)<br>
[Use Debug Diagnostics to troubleshoot a process that has stopped responding](https://support.microsoft.com/kb/919792)