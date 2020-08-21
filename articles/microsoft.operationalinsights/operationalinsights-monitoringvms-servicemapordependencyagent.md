<properties
    pageTitle="Service Map or Dependency agent"
    description="Service Map or Dependency agent"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="kinghorn"
    ms.author="kinghorn"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32745414"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="644cd5e5-d19b-476f-b2e5-4fb1461636b2"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Service Map and Dependency agent Overview

This article covers **Azure Monitor Service Map** (Service Map) and the **Dependency agent**. The Service Map solution requires that the dependency agent be installed on the VMs that intend to monitor within Service Map.  For reference, components of Service Map are now available as part of Azure Monitor for VMs.

For Questions related to the Log Analytics agent (Windows and Linux) and Azure Migrate's use of Service Map, please refer to their respective support articles. 

## **Recommended Documents**

* [Using the Service Map solution in Azure](https://docs.microsoft.com/azure/azure-monitor/insights/service-map)
* [Service Map data that can be queried in Log Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/service-map#log-analytics-records)
* [Service Map REST API information](https://docs.microsoft.com/azure/azure-monitor/insights/service-map#rest-api)
* [Azure Monitor for VMs information](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-overview)

### Solution setup and agent installation

* [Supported regions](https://docs.microsoft.com/azure/azure-monitor/insights/service-map-configure#supported-azure-regions)
* [Supported Windows operating systems](https://docs.microsoft.com/azure/azure-monitor/insights/service-map-configure#supported-windows-operating-systems)
* [Supported Linux operating systems](https://docs.microsoft.com/azure/azure-monitor/insights/service-map-configure#supported-linux-operating-systems)
* [Setup Azure VMs](https://docs.microsoft.com/azure/azure-monitor/insights/service-map-configure#installation)
* [Setup On-premises/Other cloud VMs](https://docs.microsoft.com/azure/azure-monitor/insights/service-map-configure#dependency-agent-downloads)

### SCOM Integration

* [Setup an integration with System Center Operations Manager](https://docs.microsoft.com/azure/azure-monitor/insights/service-map-scom)
* [SCOM Integration known issues and limitations](https://docs.microsoft.com/azure/azure-monitor/insights/service-map-scom#known-issues-and-limitations)

### Troubleshooting guides

* [Dependency agent installation issues](https://docs.microsoft.com/azure/azure-monitor/insights/service-map-configure#dependency-agent-installation-problems)
* [Missing data or machines not appearing in the map](https://docs.microsoft.com/azure/azure-monitor/insights/service-map-configure#post-installation-issues)
