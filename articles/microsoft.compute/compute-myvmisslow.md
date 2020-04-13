<properties
	pageTitle="Diagnose and resolve Virtual Machine performance issues"
	description="Diagnose and resolve Virtual Machine performance issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32411875"
	resourceTags="windows, windowsSQL"
	productPesIds="14749,14745"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="f41ebb73-3970-4687-80dc-8b06e4335a57"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Diagnose and resolve Virtual Machine performance issues

Try the following steps to diagnose and mitigate VM performance issues.<br>

## **Recommended Steps**

1. **Did you know Performance diagnostics can help you analyze guest VM issues?** **For Windows virtual machines, you can [run Performance diagnostics](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId)** and review results directly from the Azure portal. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [Learn more](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics)
2. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
3. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization. On **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon) tool.
4. Use VM Diagnostics and Storage Diagnostics in the Azure portal to identify if any resource is being overutilized or throttled <br>
5. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)<br>
6. Address any Azure host issues by [redeploying](data-blade:Microsoft_Azure_Compute.VirtualMachineRedeployViewModel.id.$resourceId) the VM, which migrates it to a new Azure host
7. Scale up the Virtual Machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource
8. Consider using [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage) if it's an I/O intensive use-case <br>

## **Recommended Documents**

* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
