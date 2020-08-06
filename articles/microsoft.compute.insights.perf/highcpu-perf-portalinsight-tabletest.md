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

### Performance Table

<!--$DataTable-->DataTable<!--/$DataTable-->


**What can cause CPU spike on a VM?**

* The load pattern is compute intensive, in which case the consistent spikes are expected
* Was there a recent code change which might be causing this behavior?
* Was there a recent change in number of users or spike in amount of data processing?
* Does it correlate with a job processing e.g. maintenance, indexing, cube processing, end of day reporting?
* A system process after a recent OS patch, could be driving high CPU consumption

## **Recommended Steps**

**Detection: If you are unaware of the process driving high CPU consumption, for the machine <!--$vmname-->[vmname]<!--/$vmname-->, you can [access PerfInsights here](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/performanceDiagnostics)** and review results directly from the Azure portal. You may also [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics#install-and-run-performance-diagnostics-on-your-vm) and run it in your virtual machine. PerfInishgts generates a report that contains a dedicated tab for CPU analysis.

**If it's expected due to the kind of data or user pattern, then it is recommended to resize to a higher VM SKU**. You can read more about different [Azure Virtual Machine offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/) and decide on which Virtual Machine offering best suits your workload.


## **Recommended Documents**

* [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
* [Azure Virtual Machine offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/)
