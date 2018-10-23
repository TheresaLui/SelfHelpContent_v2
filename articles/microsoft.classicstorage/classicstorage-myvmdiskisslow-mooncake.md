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
    cloudEnvironments="MoonCake"
/>

# My VM/Disk is slow

## **Recommended steps**

Try following steps to diagnose and mitigate VM performance issue.

1. **Do you know PerfInsights can help you analyze Guest VM issues?** Start here: [Download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True).<br>
    To ensure a speedy resolution, you can also provide us the PerfInsights logs if you create a support case.
2. Review your application error logs, traces and metrics to find any bottlenecks causing performance issues.<br>
    Restart Application and machine as a quick way to recover from one-time issues.
3. Review OS (Operating System) level metrics such as CPU, memory usage, IO and network to see if any resource has consistent high utilization.<br>
    For example on Windows use Perfmon.
4. Use VM Diagnostics and Storage Diagnostics in Azure Portal to identify if any resource being overutilized or throttled.<br>
    [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)
5. Scale up the Virtual Machine to a different VM type or series for increased performance<br>
    Click 'Size' in the Settings blade of the VM resource.
6. Consider using Premium Storage account if its an I/O intensive use-case.<br>
    [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.azure.cn/storage/common/storage-premium-storage/)

## **Recommended documents**

* [Detailed troubleshooting of Azure Storage](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting/)
