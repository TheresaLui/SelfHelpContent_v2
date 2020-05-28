<properties
	pageTitle="My VM is slow"
	description="My VM is slow"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds="32411877,32511162"
	resourceTags="windows, linux, windowsSQL, redhat, Ubuntu"
	productPesIds="14749,16342,14745,15571,15797,16454"
	cloudEnvironments="MoonCake, Fairfax"
	articleId="02a0e3e3-4126-4437-9f7e-ec0d495b5c1c"
	ownershipId="Compute_VirtualMachines_Content"
/>

# My VM is slow

## **Recommended steps**

Try the following steps to diagnose and mitigate VM performance issues:

1. **Did you know PerfInsights can help you analyze Windows guest VM issues?**  
	[Download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on the VM. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [Learn more](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfInsights)

2. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
3. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization.<br>
	* On **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon) tool.
	* On Linux, use commands such as Top, VmStat, Lsof, and Tcpdump.<br>


4. Use VM Diagnostics and Storage Diagnostics in the Azure portal to identify if any resource is being overutilized or throttled <br>
5. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)<br>
6. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId) the VM, which migrates it to a new Azure host.<br>
7. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource.<br>
8. Consider using [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.azure.cn/storage/storage-premium-storage/) if its an I/O intensive use-case <br>


## **Recommended documents**

* [Detailed troubleshooting of Azure Storage](https://docs.azure.cn/storage/storage-monitoring-diagnosing-troubleshooting/)
