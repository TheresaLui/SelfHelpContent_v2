<properties
    pageTitle="My VM is slow"
    description="My VM is slow "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="ScottAzure"
    ms.author="scotro"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds="32628264,32628261,32628277,32628275,32628268,32628270"
    resourceTags="windows, linux, windowsSQL, redhat"
    productPesIds="14749,15571,15797,16454"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5b164da5-bc96-47b3-8bd9-74cfcf4db851"
    category="performance"
    searchTags="slow, performance, vm"
	ownershipId="Compute_VirtualMachines_Content"
/>

# My VM is slow

Try the following steps to diagnose and mitigate VM performance issues.

## **Recommended Steps**

1. **Did you know PerfInsights can help you analyze Windows guest VM issues?**  

    [Install Azure Performance Diagnostics VM Extension](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics-vm-extension) directly from Azure portal. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run on the VM. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [Learn more](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfInsights)

2. Review your application error logs, traces, and metrics to determine if there are any application bottlenecks causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
3. Review operating system level metrics such as CPU, memory usage, IO, and network to see if any resource has consistently high utilization:

    * On **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon) tool
    * On **Linux**, use commands such as Top, VmStat, Lsof, and Tcpdump

4. Use [VM and Storage Diagnostics](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running) in the Azure portal to identify if any resource is being overutilized or throttled. You can then enable diagnostics and monitoring to troubleshoot issues with Azure VMs and Storage.
5. Restart the VM to address any VM operating system issues by clicking 'Restart' at the top of the VM resource blade
6. Scale up the virtual machine to a different VM type or series for increased performance by clicking 'Size' in the Settings blade of the VM resource
7. Consider using [Premium Storage for Azure Virtual Machine Workloads](https://docs.microsoft.com/azure/virtual-machines/windows/disks-types)

## **Recommended Documents**

* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
