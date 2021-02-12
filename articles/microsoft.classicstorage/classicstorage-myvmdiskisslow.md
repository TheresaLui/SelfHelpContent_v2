<properties
	pageTitle="My VM/Disk is slow"
	description="My VM/Disk is slow"
	service="microsoft.classicstorage"
	resource="storageaccounts"
	authors="kasparks"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="69c0d115-63b1-47ef-80a9-fe664b9507e0"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# My VM/Disk is slow

## **Recommended steps**
Try following steps to diagnose and mitigate VM performance issues:

1. **Did you know PerfInsights can help you analyze Windows guest VM issues?**  
	[Install Azure Performance Diagnostics VM Extension](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics-vm-extension) directly from Azure portal. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run on the VM. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [Learn more](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfInsights)

2. Review your application error logs, traces and metrics to find any bottlenecks causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
3. Review OS (Operating System) level metrics such as CPU, memory usage, IO and network to see if any resource has consistent high utilization. 
For example on **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon) tool.
4. Use [VM and Storage Diagnostics](http://aka.ms/azurevmperf) in the Azure portal to identify if any resource is being overutilized or throttled. You can then enable diagnostics and monitoring to troubleshoot issues with Azure VMs and Storage.
5. Scale up the Virtual Machine to a different VM type or series for increased performance<br>
Click 'Size' in the Settings blade of the VM resource.
6. Consider using Premium Storage account if its an I/O intensive use-case.<br>
[Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://azure.microsoft.com/documentation/articles/storage-premium-storage-preview-portal/)


## **Recommended documents**
[Detailed troubleshooting of Azure Storage](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/)
