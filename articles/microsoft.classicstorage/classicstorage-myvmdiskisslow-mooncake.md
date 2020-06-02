<properties
    pageTitle="My VM/Disk is slow"
    description="My VM/Disk is slow"
    service="microsoft.classicstorage"
    resource="storageaccounts"
    authors="kasparks"
    ms.author="kasparks"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15629"
    cloudEnvironments="MoonCake"
	articleId="49cb4f69-ed79-4966-9d3a-d4a5bffa046d"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# My VM/Disk is slow

## **Recommended Steps**

Try the following steps to diagnose and mitigate VM performance issues:

1. **Did you know PerfInsights can help you analyze Windows guest VM issues?**  [Download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on the VM. To ensure a speedy resolution, provide the PerfInsights logs if you create a support case.
2. Review your application error logs, traces, and metrics to find any bottlenecks causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
3. Review OS (Operating System) level metrics such as CPU, memory usage, IO, and network to see if any resource has consistent high utilization. For example, on **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon) tool.
4. Use [VM and Storage Diagnostics](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running) in the Azure portal to identify if any resource is being overutilized or throttled. You can then enable diagnostics and monitoring to troubleshoot issues with Azure VMs and Storage.
5. Scale up the Virtual Machine to a different VM type or series for increased performance. Click 'Size' in the Settings blade of the VM resource.
6. Consider using Premium Storage account you have an I/O intensive use-case. [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.azure.cn/storage/common/storage-premium-storage/)

## **Recommended Documents**

* [Detailed troubleshooting of Azure Storage](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting/)
