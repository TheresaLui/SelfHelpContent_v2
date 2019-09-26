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
    cloudEnvironments="public"
/>

# Perfinsights Diagnostics Tool is not installed

<!--issueDescription-->
**Do you know Perfinsights tool could help you diagnose key performance issues on this VM?**

We have detected that Perfinsights is not installed on - <!--$vmname-->[vmname]<!--/$vmname-->

Perfinsights is a diagnostics tool which can help you analyze operating system level metrics such as:

1. Best Practices recommendations for SQL and Windows
2. Top CPU consumers
3. Top Memory consumers
4. Key IO metrics, with Disk level IOPS/Mbps graphs
5. Storage Pool layout

<!--/issueDescription-->

## **Recommended Steps**
**For the machine <!--$vmname-->[vmname]<!--/$vmname-->, you can [Install PerfInsights](data-blade:Microsoft_Azure_Compute.PerformanceDiagnosticsBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/performanceDiagnostics)** and review results directly from the Azure portal. You may also [download PerfInsights](https://www.microsoft.com/download/details.aspx?id=54915&fa43d42b-25b5-4a42-fe9b-1634f450f5ee=True) and run it on your virtual machine. To ensure a speedy resolution, provide us the PerfInsights logs if you create a support case. [How to use PerfInsights](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/how-to-use-perfinsights)
