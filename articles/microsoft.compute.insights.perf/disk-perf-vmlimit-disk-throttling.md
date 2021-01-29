<properties
    pageTitle="Recent instances of VM reaching disk IO limits detected"
    description="Recent instances of VM reaching disk IO limits detected"
    infoBubbleText="Recent instances of VM reaching disk IO limits detected"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="tibasham"
    displayOrder=""
    articleId="diskthrottling-vmlimit"
    diagnosticScenario="Recent instances of VM reaching disk IO limits detected"
    selfHelpType="diagnostics"
    supportTopicIds="32628264,32628261,32628277,32628275,32628268,32628270,32633490,32633512,32633522,32633524,32633527"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# **The VM appears to have reached it's disk IO limits recently**

## **There were recent instances of the <!--$vmname-->[vmname]<!--/$vmname--> reaching its disk IO limits.**

<!--issueDescription-->
Our diagnostics show there were recent instances where the VM <!--$vmname-->[vmname]<!--/$vmname--> reached the <!--$diskType-->disktype<!--/$diskType--> disk <!--$throttlingCounter-->Counter<!--/$throttlingCounter-->. The current <!--$throttlingCounter-->Counter<!--/$throttlingCounter--> limit for this  (<!--$vmType-->VMSize<!--/$vmType-->) VM is (<!--$vmLimit-->limit<!--/$vmLimit-->).
<!--/issueDescription-->

### Recent instances of the VM reaching its disk IO limits

<!--$DataTable-->DataTable<!--/$DataTable-->

## Diagnose and resolve Virtual Machine disk performance issues

Azure virtual machines have IOPS and throughput performance limits based on the virtual machine type and size. When your application running on your virtual machine requests more IOPS or throughput than what is allotted for the virtual machine, your application's performance is capped. When this happens, the application will experience suboptimal performance and can lead to negative consequences, such as increased latency.

## **Recommended Steps**

If you are experiencing issues with disk performance, see our guidance on [Windows Virtual Machines and disk performance](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows).

**Detection: If you are unaware of the process driving disk consumption, for Windows virtual machines**, [run PerfInsights](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/performanceDiagnostics) and review results directly from the Azure portal. PerfInsights generates a report that contains a dedicated tab for storage analysis.

You can also [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics#install-and-run-performance-diagnostics-on-your-vm) and run it in your virtual machine. 

*If you proceed to open a support case, attach the PerfInsights report for the Support Engineer to analyze.*

### Additional tools and guidance for troubleshooting disk performance

1. [Enable diagnostics, monitor, identify and remediate issues with Azure VMs and storage](https://support.microsoft.com/help/3150851/generic-performance-troubleshooting-for-azure-virtual-machine-running)
1. Review your application error logs, traces, and metrics to determine if any application level bottlenecks are causing performance issues. As a quick way to recover from one-time issues, restart your application and virtual machine.
1. Review operating system level metrics such as IO, CPU, memory usage, and network to see if any resource has consistently high utilization. On **Windows**, use the [Perfmon](https://docs.microsoft.com/windows-server/administration/windows-commands/perfmon), and [Iometer](https://docs.microsoft.com/azure/virtual-machines/windows/disks-benchmarks#iometer)
1. Address any Azure host issues by [redeploying](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows) the VM, which migrates it to a new Azure host
1. Scale up the virtual machine to a different VM type or series for increased performance by clicking **Size** in the **Settings** blade of the VM. For more information, see [Storage optimized VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes-storage)
1. If your workload is I/O intensive, consider using [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage-performance)
1. Consider using Premium SSDs for [flexibility to increase disk performance without increasing the actual disk size](https://docs.microsoft.com/azure/virtual-machines/disks-performance-tiers?toc=/azure/virtual-machines/windows/toc.json)

## **Recommended Documents**
 
* [Windows Virtual Machines and disk performance](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows)
* [Benchmarking disks in Azure Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/disks-benchmarks)
* [Detailed troubleshooting of Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting)
* [Azure Virtual Machine Sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes)
* [Azure Compute benchmark scores for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/compute-benchmark-scores)
* [Optimize network throughput for Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-optimize-network-bandwidth)
* [SQL Performance guidelines for Azure VMs](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)
