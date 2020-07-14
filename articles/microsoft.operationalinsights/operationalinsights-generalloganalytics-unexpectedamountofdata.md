
<properties
pageTitle="Unexpected amount of data ingested"
description="Unexpected amount of data ingested"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="yossiy"
ms.author="yossiy"
displayorder="13"
selfHelpType="resource"
supportTopicIds="32612527"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	articleId="28a925f0-2bd9-4ba3-9bca-ee3c53e2b869"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Unexpected amount of data ingested

**How do I understand the source of my ingested data volume?**<br>

For a quick view of recent data ingestion trends, go to the Log Analytics page “Usage and estimated costs” from your workspace’s left navigation. Here you can see your daily trend of data ingestion by solution where you can look for changes in your data ingestion patterns – e.g. the addition of a new solution or higher data volumes per solution ([learn more](https://docs.microsoft.com/azure/azure-monitor/platform/data-usage)). To investigate further, query for the number of nodes sending data and which nodes are sending the most. The queries needed for this investigation can be found [here](https://docs.microsoft.com/azure/azure-monitor/platform/data-usage?toc=%2Fazure%2Fazure-monitor%2Ftoc.json#troubleshooting-why-usage-is-higher-than-expected). Finally, to avoid surprises, you can [set up an alert](https://docs.microsoft.com/azure/azure-monitor/platform/data-usage?toc=%2Fazure%2Fazure-monitor%2Ftoc.json#create-an-alert-when-data-collection-is-higher-than-expected) so you’ll know about higher-than-usual data volumes.


## **Recommended Documents**

* [New pricing model and Operations Management Suite subscription entitlements](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model-and-operations-management-suite-subscription-entitlements)
* [Moving to the new pricing model](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#moving-to-the-new-pricing-model)
* [Managing access to Log Analytics using Azure permissions](https://docs.microsoft.com/azure/log-analytics/log-analytics-manage-access?toc=/azure/azure-monitor/toc.json#managing-access-to-log-analytics-using-azure-permissions)
* [Troubleshoot why your usage is higher than expected](https://docs.microsoft.com/azure/azure-monitor/platform/data-usage#troubleshooting-why-usage-is-higher-than-expected)
* [Create an alert when data collection is higher than expected](https://docs.microsoft.com/azure/azure-monitor/platform/data-usage#create-an-alert-when-data-collection-is-higher-than-expected)
