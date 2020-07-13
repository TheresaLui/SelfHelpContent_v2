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

Sometimes even after enabling Application Insights Snapshot Debugger for your application, you still don’t see snapshots for exceptions, or they seem incorrect. There can be many different reasons why snapshots are not generated. Please see below Recommended Steps:

## **Recommended Steps**

### 1. **Ensure the Snapshot is enabled** 

* if Application is running in Azure App Service then follow the steps mentioned in this [link](https://docs.microsoft.com/azure/azure-monitor/app/snapshot-debugger-appservice) to ensure its enabled.
* if your application requires a customized Snapshot Debugger configuration, or a preview version of .NET core, then [this instruction](https://docs.microsoft.com/azure/azure-monitor/app/snapshot-debugger-vm?toc=/azure/azure-monitor/toc.json) should be followed **in addition** to the instructions for [enabling through the Application Insights portal page](https://docs.microsoft.com/azure/azure-monitor/app/snapshot-debugger-appservice?toc=/azure/azure-monitor/toc.json).
* if your application runs in Azure Service Fabric, Cloud Service, Virtual Machines, or on-premises machines verify that you have enabled its via steps [mentioned here](https://docs.microsoft.com/azure/azure-monitor/app/snapshot-debugger-vm). 

### 2. **If the Snapshots were collected but went missing recently** 

* Navigate to Failures page and click on the **Snapshot only** checkbox to view if snapshots are being collected. Expand the time range to see when they stopped collecting. Refer to this [troubleshooting guide](https://docs.microsoft.com/azure/azure-monitor/app/snapshot-debugger-troubleshoot).  

![appmap image](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/app-insights/application-insights-snapshot-debugger-is-missing.png)


### 3. **Ensure you have permissions** 

* Access to snapshots is protected by role-based access control (RBAC). To inspect a snapshot, you must first be added to the necessary role by a subscription owner. Follow [this link](https://docs.microsoft.com/azure/azure-monitor/app/snapshot-debugger#grant-permissions) to ensure permissions. 

### 4. **Use the snapshot health check** 

* Use the Snapshot Health Check to troubleshoot common problems like using an outdated Snapshot Collector, reaching the daily upload limit, or perhaps the snapshot is just taking a long time to upload. Follow the [instructions here](https://docs.microsoft.com/azure/azure-monitor/app/snapshot-debugger-troubleshoot) to use the health check.


## **Recommended Documents**

* [Snapshot Debugger Troubleshooting Guide](https://docs.microsoft.com/azure/azure-monitor/app/snapshot-debugger-troubleshoot)<br>
* [Debug snapshots on exceptions in .NET apps](https://go.microsoft.com/fwlink/?linkid=848053)<br>
* [Diagnose exceptions in your web apps with Application Insights.](https://go.microsoft.com/fwlink/?linkid=867931)<br>