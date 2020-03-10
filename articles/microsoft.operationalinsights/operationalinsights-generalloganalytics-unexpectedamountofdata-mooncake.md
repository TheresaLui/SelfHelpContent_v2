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
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="operationalinsights-generalloganalytics-unexpectedamountofdata-mooncake"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# Unexpected amount of data ingested

**How do I understand the source of my ingested data volume?**

For a quick view of recent data ingestion trends, go to the Log Analytics page "Usage and estimated costs" from your workspace's left navigation. Here you can see your daily trend of data ingestion by solution where you can look for changes in your data ingestion patterns – e.g. the addition of a new solution or higher data volumes per solution ([learn more](https://docs.azure.cn/azure-monitor/platform/manage-cost-storage)). To investigate further, query for the number of nodes sending data and which nodes are sending the most. The queries needed for this investigation can be found [here](https://docs.azure.cn/azure-monitor/platform/manage-cost-storage?toc=%2Fazure%2Fazure-monitor%2Ftoc.json#troubleshooting-why-usage-is-higher-than-expected). Finally, to avoid surprises, you can [set up an alert](https://docs.azure.cn/azure-monitor/platform/manage-cost-storage?toc=%2Fazure%2Fazure-monitor%2Ftoc.json#create-an-alert-when-data-collection-is-higher-than-expected) so you'll know about higher-than-usual data volumes.


## **Recommended Documents**

* [New pricing model and Operations Management Suite subscription entitlements](https://docs.azure.cn/azure-monitor/platform/usage-estimated-costs#new-pricing-model-and-operations-management-suite-subscription-entitlements)
* [Moving to the new pricing model](https://docs.azure.cn/azure-monitor/platform/usage-estimated-costs#moving-to-the-new-pricing-model)
* [Managing access to Log Analytics using Azure permissions](https://docs.azure.cn/azure-monitor/platform/manage-access?toc=%2Fazure%2Fazure-monitor%2Ftoc.json#managing-access-to-log-analytics-using-azure-permissions)
* [Troubleshoot why your usage is higher than expected](https://docs.azure.cn/azure-monitor/platform/manage-cost-storage#troubleshooting-why-usage-is-higher-than-expected)
* [Create an alert when data collection is higher than expected](https://docs.azure.cn/azure-monitor/platform/manage-cost-storage#create-an-alert-when-data-collection-is-higher-than-expected)
