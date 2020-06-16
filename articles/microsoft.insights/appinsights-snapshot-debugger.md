<properties
    pageTitle="Snapshot Debugger captures are incorrect or missing"
    description="MSnapshot Debugger captures are incorrect or missing"
    service="microsoft.insights"
    resource="components"
    authors="rishabjolly"
    ms.author="rijolly"
    displayOrder="2"
    articleId="appinsights-snapshot-debugger"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32729632"
    resourceTags=""
    productPesIds="15693"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# <-- Snapshot-Debugger-captures-are-incorrect-or-missing -->

Sometimes even after enabling Application Insights Snapshot Debugger for your application, you still don’t see snapshots for exceptions, or they seem incorrect. There can be many different reasons why snapshots are not generated. Please see below recommended solutions:

## **Recommended solutions**

### 1. **Ensure the Snapshot is enabled** 

* if Application is running in Azure App Service then follow the steps mentioned in this [link](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-appservice) to ensure its enabled.
* if your application requires a customized Snapshot Debugger configuration, or a preview version of .NET core, then [this instruction](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-vm?toc=/azure/azure-monitor/toc.json) should be followed **in addition** to the instructions for [enabling through the Application Insights portal page](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-appservice?toc=/azure/azure-monitor/toc.json).
* if your application runs in Azure Service Fabric, Cloud Service, Virtual Machines, or on-premises machines verify that you have enabled its via steps [mentioned here](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-vm). 

### 2. **Ensure the Snapshot is enabled** 

* Access to snapshots is protected by role-based access control (RBAC). To inspect a snapshot, you must first be added to the necessary role by a subscription owner. Follow [this link](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger#grant-permissions) to ensure permissions. 

### 3. **Ensure the Snapshot is enabled** 

* Use the Snapshot Health Check to troubleshoot common problems like using an outdated Snapshot Collector, reaching the daily upload limit, or perhaps the snapshot is just taking a long time to upload. Follow the [instructions here](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-troubleshoot) to use the health check.

### 4. **Ensure the Snapshot is enabled** 

* Make sure you're using the correct instrumentation key in your published application. Usually, the instrumentation key is read from the ApplicationInsights.config file. Verify the value is the same as the instrumentation key for the Application Insights resource that you see in the portal.

### 5. **Ensure the Snapshot is enabled** 

* Follow [this link](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-troubleshoot#preview-versions-of-net-core) to get the latest version of the NuGet package

### 6. **Ensure the Snapshot is enabled** 

* You can get details on how to check the uploader logs for your apps hosted on App Service and other environments [here](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-troubleshoot#check-the-uploader-logs) .

### 7. **Ensure the Snapshot is enabled** 

* For roles in Cloud Services, the default temporary folder may be too small to hold the minidump files, leading to lost snapshots. The space needed depends on the total working set of your application and the number of concurrent snapshots. Get details on [this link](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-troubleshoot#troubleshooting-cloud-services) to further troubleshoot.

### 8. **Ensure the Snapshot is enabled** 

* When the Snapshot Collector starts up, it tries to find a folder on disk that is suitable for running the Snapshot Uploader process. The chosen folder is known as the Shadow Copy folder. To work around any errors pertaining to Shadow Copy folder, follow [instruction in this link](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-troubleshoot#overriding-the-shadow-copy-folder)

### 9. **Ensure the Snapshot is enabled** 

* When a snapshot is created, the throwing exception is tagged with a snapshot ID Using Search in Application Insights, you can find all telemetry with the ai.snapshot.id custom property. Follow [these instruction](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-troubleshoot#use-application-insights-search-to-find-exceptions-with-snapshots)

### 10. **Ensure the Snapshot is enabled** 

* If your application connects to the Internet via a proxy or a firewall, you may need to edit the rules to allow your application to communicate with the Snapshot Debugger service. The IPs used by Snapshot Debugger are included in the Azure Monitor service tag

## **Recommended Documents**

* [Snapshot Debugger Troubleshooting Guide](https://docs.microsoft.com/en-us/azure/azure-monitor/app/snapshot-debugger-troubleshoot)<br>
* [Debug snapshots on exceptions in .NET apps](https://go.microsoft.com/fwlink/?linkid=848053)<br>
* [Diagnose exceptions in your web apps with Application Insights.](https://go.microsoft.com/fwlink/?linkid=867931)<br>