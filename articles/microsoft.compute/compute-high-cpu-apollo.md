<properties
    pageTitle="Troubleshooting High CPU for an Azure Virtual Machine"
    description="Troubleshooting High CPU for an Azure Virtual Machine"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    ms.author="mahuss"
    displayOrder="0"
    articleId="024da352-807e-475b-b8ae-68f42be8d2b6"
    selfHelpType="Apollo"
    supportTopicIds="8b618100-f5cd-7ad5-1c69-72aaf37d801d, 5a5377ad-0f05-a3ba-d25e-98346a3f74df"
    productPesIds="14749, 15571"
    resourceTags="windows"
    cloudEnvironments="public"
    ownershipId="Compute_VirtualMachines_Content"
/>

# Troubleshooting High CPU for an Azure Virtual Machine

## **Troubleshooting High CPU Usage for an Azure Virtual Machine**

:::Section Metrics and Diagnostics:::

Review the graph to see the CPU usage as it correlates to your workload. Identify any patterns or spikes that are tied to the load, scheduled jobs, or unexpected consumption of resources.

<metric>
    <name>Percentage CPU</name>
    <aggregationType>Avg</aggregationType>
    <timeSpanDuration>1d</timeSpanDuration>
    <title>Current Virtual Machine CPU Usage</title>
</metric>

### VM Performance Diagnostics

We are attempting to run diagnostics for your Azure Virtual Machine. If any issues are detected, the findings will be listed below.
 
<Insight>
    <symptomId>HighCpuUsageAzurePortalInsight,VMPerfDiagExtAzurePortalInsight</symptomId>
    <executionText>We are running a few performance checks on your VM</executionText>
    <timeoutText>This check was taking too long, so we stopped the operation</timeoutText>
    <noResultText>No issues found</noResultText>
    <additionalInputsReq>false</additionalInputsReq>
</Insight>

**What can cause CPU spike on a VM?**

High CPU can indicate that the application is performing many CPU-intensive tasks relative to the incoming load. This can indicate that a component used by this application uses is unable to process data as efficiently as expected, that there might be a code issue, or that there are insufficient resources to handle the load that the application is handling. Here are some common factors leading to high CPU:  

1. A recent code change or deployment. This is mostly applicable to apps like IIS, SharePoint, SQL, or third-pary applications.
1. A recent patch, which could be related to an OS level patch, or Application level cumulative patches/fixes.
1. Query change or outdated Indexes: SQL or Oracle data tier application also have query plan optimization as another factor. Lack of proper indexes, data changes, and so on,  sometimes lead to some queries getting more compute intensive. 
1. Azure VM-specific: there are certain processes like RDAgent, Extension specific processes (Monitoring Agent, MMA agent, Security client exe, and so on) that sometimes lead to High CPU consumption and needs to be looked from configuration or known issues perspective.  

See [Troubleshoot high-CPU issues for Azure Windows virtual machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-high-cpu-issues-azure-windows-vm)

## **Recommended Steps**

**Detection: If you are unaware of the process driving high CPU consumption, for the machine <!--$vmname-->[vmname]<!--/$vmname-->, you can [access PerfInsights here](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/performanceDiagnostics)** and review results directly from the Azure Portal. PerfInsights generates a report that contains a dedicated tab for CPU analysis. The report lists the processes per Average CPU consumption in descending order. It will indicate if the process was system-based or related to Microsoft-owned App (SQL, IIS) or a third-party process. We have a dedicated sub-tab under CPU that can be leveraged for detailed pattern analysis, per core, or per process.

You may also [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics#install-and-run-performance-diagnostics-on-your-vm) and run it in your virtual machine.   

There are two broad approaches to resolving high CPU issues depending upon whether the CPU usage is appropriate given the application load or because of a bug within the application:

1.	If it's likely due to the kind of data or user pattern, we recommend resizing to a higher VM SKU**. You can read more about different [Azure Virtual Machine offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/) and decide on which Virtual Machine offering best suits your workload. 
1.	If high CPU is caused due to an application issue, then improving the efficiency of the current application by analyzing the code for potential improvements can help resolve the issue. If the identified application is a third-party application, then you would need to engage the vendor/developer of the application. 

If you are unable to access your virtual machine via RDP or SSH you can try restarting to temporarily regain access, then proceed to troubleshoot using [PerfInsights](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/performanceDiagnostics) to determine what is causing the CPU spike.

**If you proceed to open a support case, attach the PerfInsights report for the Support Engineer to analyze.**

## **Recommended Documents**

* [Troubleshoot high-CPU issues for Azure Windows virtual machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-high-cpu-issues-azure-windows-vm)
* [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
* [Azure Virtual Machine offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/)
* [Performance guidelines for SQL Server](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices)
