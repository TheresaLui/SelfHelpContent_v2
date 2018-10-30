<properties
	pageTitle="My VM is slow"
	description="My VM is slow"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32411877,32511162"
	resourceTags="linux, redhat, Ubuntu"
	productPesIds="16342,15571,15797,16454"
	cloudEnvironments="public"
/>

# My VM is slow

## **Recommended steps**

Try the following steps to diagnose and mitigate VM performance issues:

1. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
2. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization.<br>

	* Use commands such as Top, VmStat, Lsof, and Tcpdump.<br>

3. Use VM Diagnostics and Storage Diagnostics in the Azure portal to identify if any resource is being overutilized or throttled <br>
4. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)<br>
5. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId) the VM, which migrates it to a new Azure host.<br>
6. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource.<br>
7. Consider using [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.azure.cn/storage/storage-premium-storage/) if its an I/O intensive use-case <br>


## **Recommended documents**

* [Detailed troubleshooting of Azure Storage](https://docs.azure.cn/storage/storage-monitoring-diagnosing-troubleshooting/)
