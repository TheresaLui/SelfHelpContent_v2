<properties
    pageTitle="Perfinsights is available to run Diagnostics"
    description="Perfinsights is available to run Diagnostics"
    infoBubbleText="Perfinsights is available for your VM to run Diagnostics reports"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="MukeshNandaMS"
    ms.author="mnanda"
    displayOrder=""
    articleId="perfinsights-available-windows"
    diagnosticScenario="PerfInsights available to run Diagnostics"
    selfHelpType="diagnostics"
    supportTopicIds="32628264,32628261,32628277,32628275,32628268,32628270,32633490,32633512,32633522,32633524,32633527"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# PerfInsights is available to run performance reports for your VM

<!--issueDescription-->
We have detected that PerfInsights is already installed on your VM. You can run PerfInsights on-demand through the Portal and view reports for your analysis.
<!--/issueDescription-->

PerfInsights is a diagnostics tool that can help you analyze operating system level metrics such as: 

* Best Practices recommendations for SQL and Windows
* Top CPU consumers
* Top Memory consumers
* Key IO metrics, with Disk level IOPS/Mbps graphs
* Storage Pool layout

## **Recommended Steps**

**For the machine <!--$vmname-->[vmname]<!--/$vmname-->, you can [access PerfInsights here](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/performanceDiagnostics)** and review results directly in the Azure portal. 

You may also [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics#install-and-run-performance-diagnostics-on-your-vm) and run it on your virtual machine.

**If you proceed to open a support case please attach the PerfInsights report for the Support Engineer to analyze.**

## **Recommended Documents**

* [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
