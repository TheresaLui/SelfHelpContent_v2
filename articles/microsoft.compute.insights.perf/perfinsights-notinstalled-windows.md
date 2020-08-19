<properties
    pageTitle="Perfinsights Not Installed"
    description="Perfinsights Not Installed"
    infoBubbleText="Install Perfinsights to run detailed Performance diagnostics reports"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="MukeshNandaMS"
    ms.author="mnanda"
    displayOrder=""
    articleId="perfinsights-notinstalled-windows"
    diagnosticScenario="Perfinsights not installed"
    selfHelpType="diagnostics"
    supportTopicIds="32628264,32628261,32628277,32628275,32628268,32628270,32633490,32633512,32633522,32633524,32633527"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# PerfInsights tool can help you diagnose key performance issues on this VM

<!--issueDescription-->
We have detected that PerfInsights is not installed on your VM. Perfinsights can help you diagnose key performance issues on your VM. 
<!--/issueDescription-->

PerfInsights is a diagnostics tool that can help you analyze operating system level metrics such as: 

* Best Practices recommendations for SQL and Windows
* Top CPU consumers
* Top Memory consumers
* Key IO metrics, with Disk level IOPS/Mbps graphs
* Storage Pool layout

## **Recommended Steps**

**For the machine <!--$vmname-->[vmname]<!--/$vmname-->, you can [Install PerfInsights](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/performanceDiagnostics)** and review results directly in the Azure portal. 

You may also [download PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/performance-diagnostics#install-and-run-performance-diagnostics-on-your-vm) and run it on your virtual machine. 

**If you proceed to open a support case please attach the PerfInsights report for the Support Engineer to analyze.**

## **Recommended Documents**

* [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
