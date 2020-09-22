<properties
	pageTitle="My VM/Disk is slow"
	description="Diagnose and mitigate VM performance issues"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="kasparks,anandhms"
	displayOrder="50"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	ms.author="anandh"
	cloudEnvironments="MoonCake"
	articleId="storage-myvmdiskisslow-mooncake"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# My VM/Disk is slow

## **Recommended Steps**

Try the following steps to diagnose and mitigate VM performance issues:

1. **Did you know Performance diagnostics can help you analyze guest VM issues?**  For Windows virtual machines, you can [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case.
2. Review your application error logs, traces, and metrics to find any bottlenecks causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
3. Review OS (Operating System) level metrics such as CPU, memory usage, IO, and network to see if any resource has consistent high utilization. For example, on **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon) tool.
4. Use [VM and Storage Diagnostics](http://aka.ms/azurevmperf) in the Azure portal to identify if any resource is being overutilized or throttled. You can then enable diagnostics and monitoring to troubleshoot issues with Azure VMs and Storage.
5. Scale up the Virtual Machine to a different VM type or series for increased performance. Click 'Size' in the Settings blade of the VM resource.
6. Consider using Premium Storage account if its an I/O intensive use-case. [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.azure.cn/virtual-machines/windows/disks-types#premium-ssd)

## **Recommended Documents**

* [Detailed troubleshooting of Azure Storage](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting)