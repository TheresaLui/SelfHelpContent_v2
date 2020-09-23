<properties
    pageTitle="Instances of High CPU detected on this VM in last 24 hrs"
    description="Instances of High CPU detected on this VM in last 24 hrs"
    infoBubbleText="Instances of High CPU detected on this VM in last 24 hrs"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="MukeshNandaMS,timbasham"
    ms.author="mnanda,tibasham"
    displayOrder=""
    articleId="cctestperftable"
    diagnosticScenario="Instances of High CPU detected on this VM in last 24 hrs"
    selfHelpType="diagnostics"
    supportTopicIds="32628264,32628261,32628277,32628275,32628268,32628270,32633490,32633512,32633522,32633524,32633527"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# **Instances of High CPU detected on the VM in last 24 hrs**

## **Do you know there were several High CPU instances on this <!--$vmname-->[vmname]<!--/$vmname--> in last 24 hrs?**

<!--issueDescription-->
Our diagnostics show there were several instances where Average Max CPU counter on this VM was above 85%. The calculations are based on Average Max CPU counter data for last 24 hrs, where it has been consistently above 85% for in 10 minute time window.
<!--/issueDescription-->

### Recent instances of High CPU usage table

<!--$DataTable-->DataTable<!--/$DataTable-->

**What can cause CPU spike on a VM?**

High CPU can indicate that the application is performing many CPU-intensive tasks relative to the incoming load. This can be an indication that a component used by this application uses is unable to process data as efficiently as expected, that there might be a code issue , or that there are insufficient resources to handle the load that the application is handling. Here are some common factors leading to high CPU:  
1.	A recent code change or deployment – Mostly applicable to apps like IIS, SharePoint, SQL or Third-Party applications 
1.	A recent patch – This could be related to OS level patch, Application level cumulative patches/fixes. 
1.	Query change or outdated Indexes – SQL or Oracle data tier application also have query plan optimization as another factor. Lack of proper indexes, Data changes etc. sometimes lead to some queries getting more compute intensive. 
1.	Azure VM Specific – There are certain processes like RDAgent, Extension specific processes (Monitoring Agent, MMA agent, Security client exe etc.) which sometimes lead to High CPU consumption and needs to be looked from configuration or known issues perspective.  

## **Recommended Steps**

**Detection: If you are unaware of the process driving high CPU consumption, for the machine <!--$vmname-->[vmname]<!--/$vmname-->, you can [access PerfInsights here](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/performanceDiagnostics)** and review results directly from the Azure portal. PerfInsights generates a report that contains a dedicated tab for CPU analysis.  It will list out the processes per Average CPU consumption in descending order. It will show point out if the process was a System or related to Microsoft owned App (SQL, IIS) or a Third-Party process. We have a dedicated Sub-Tab under CPU which could be leveraged for detailed pattern analysis, per core, or per process.

You may also [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics#install-and-run-performance-diagnostics-on-your-vm) and run it in your virtual machine.   

There are two broad approaches to resolving high CPU issues depending upon whether the CPU usage is appropriate given the application load or because of a bug within the application. 
1.	If it's expected due to the kind of data or user pattern, then it is recommended to resize to a higher VM SKU**. You can read more about different [Azure Virtual Machine offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/) and decide on which Virtual Machine offering best suits your workload. 
1.	If high CPU is caused due to an application issue, then improving the efficiency of the current application by analyzing the code for potential improvements can help resolve the issue. If the identified application is a third-party application, then you would need to engage the vendor/developer of the application. 

If you are unable to access your virtual machine via RDP or SSH you can try restarting to temporarily regain access, then proceed to troubleshoot using [PerfInsights](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/performanceDiagnostics) to determine what is causing the CPU spike.

**If you proceed to open a support case please attach the PerfInsights report for the Support Engineer to analyze.**

## **Recommended Documents**

* [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
* [Azure Virtual Machine offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/)
* [Performance guidelines for SQL Server](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices)
