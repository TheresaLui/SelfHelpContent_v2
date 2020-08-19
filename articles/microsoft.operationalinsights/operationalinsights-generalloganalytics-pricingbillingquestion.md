<properties
  pagetitle="Billing, data volume and retention"
  service="microsoft.operationalinsights"
  resource="workspaces"
  ms.author="yossiy,shemers,dalek"
  selfhelptype="Resource"
  supporttopicids="32612512"
  resourcetags=""
  productpesids="15725"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="29181eef-5603-4200-8acf-ae7d5317aaa9"
  ownershipid="AzureMonitoring_LogAnalytics" />
# Billing, data volume and retention

## How can I understand my workspace’s usage?

The Log Analytics page 'Usage and estimated costs' has information on your estimated monthly costs based on the last 30 days of usage. Additionally, there is a chart of billable data volume ingested so you can see any trends and information on which solutions account for the most data volume. From your workspace, click 'Usage and estimated costs' on the left navigation pane to see information on your [estimated monthly costs](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#understand-your-usage-and-estimate-costs) based on the last 30 days of usage. 

To learn more about the source of your workspace's data volume, review [these queries](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#troubleshooting-why-usage-is-higher-than-expected).

## **Recommended Documents**
* [Usage and estimated costs](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#understand-your-usage-and-estimate-costs)
* [Understanding the source of your workspace’s data ingestion](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#understanding-ingested-data-volume)
* [Understand what nodes are sending data](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#understanding-nodes-sending-data)
* [Tips for reducing data volume](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#tips-for-reducing-data-volume)
* [Log Analytics pricing model](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#pricing-model)
* [Azure Monitor pricing](https://azure.microsoft.com/pricing/details/monitor/)

## How can I understand my workspace’s billed costs? 

To understand what you have actually been billed, Azure provides a great deal of useful functionality in the [Azure Cost Management + Billing](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis?toc=/azure/billing/TOC.json) hub. For instance, the 'Cost analysis' functionality enables you to view your spends for Azure resources. Adding a filter by resource type (to microsoft.operationalinsights/workspace for Log Analytics) will allow you to track your spend. 

Additional understanding of your usage can be gained by [downloading your usage from the Azure portal](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date#download-usage-in-azure-portal). In the downloaded spreadsheet you can see usage per Azure resource (e.g. Log Analytics workspace) per day. In this Excel spreadsheet, usage from your Log Analytics workspaces can be found by first filtering on the 'Meter Category' column to show 'Insights and Analytics' (used by some of the legacy pricing tiers) and 'Log Analytics', and then adding a filter on the 'Instance ID' column which is 'contains workspace'. The usage is shown in the 'Consumed Quantity' column and the unit for each entry is shown in the 'Unit of Measure' column. More details are available to help you [understand your Microsoft Azure bill](https://docs.microsoft.com/azure/billing/billing-understand-your-bill) and [its Log Analytics details](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#viewing-log-analytics-usage-on-your-azure-bill). 

## **Recommended Documents**
* [Azure Monitor pricing](https://azure.microsoft.com/pricing/details/monitor/)
* [Viewing Log Analytics usage on your Azure Bill](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#viewing-log-analytics-usage-on-your-azure-bill)
* [Legacy pricing tiers](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers)

## How can I select the best pricing tier for my workspace?

In the Azure portal, open **Usage and estimated costs** from your workspace where you'll see a list of each of the pricing tiers available to your workspace. Review the estimated costs if the workspace were in each of the pricing tiers based on the last 31 days of usage. This will guide you to the most cost-effective pricing tier. Note that if you own OMS Suite licenses, you should put your workspace into the legacy Per Node pricing tier to leverage your licenses. If your workspace has access to the legacy Per Node pricing tier, you can evaluate whether this is a good choice for you using [this query](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#evaluating-the-legacy-per-node-pricing-tier).  [Learn more](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#changing-pricing-tier) about choosing a Log Analytics pricing tier. 

## **Recommended Documents**
* [Changing pricing tiers](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#changing-pricing-tier)
* [Log Analytics pricing model](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#pricing-model)
* [Legacy pricing tiers](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers)
* [Azure Monitor pricing](https://azure.microsoft.com/pricing/details/monitor/)


## How can I configure my workspace’s data retention?

To set the default retention for your workspace, from your workspace, select **Usage and estimated costs** from the left pane. On the **Usage and estimated costs** page, click **Data Retention** from the top of the page. On the pane, move the slider to increase or decrease the number of days and then click **OK**. You can also [set data retention by data type](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#retention-by-data-type) using Azure Resource Manager. If you are on the legacy Free tier, you will not be able to modify the data retention period and you need to change pricing tiers in order to control this setting. Note that there are charges for additional retention (see details on the [Azure Monitor pricing page](https://azure.microsoft.com/pricing/details/monitor/).) Also, note that the Log Analytics purge API will not reduce costs from data retention. To reduce costs, you must reduced the retention on your workspace or on specific data types in your workspace.  

## **Recommended Documents**
* [Managing your workspace’s data retention](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#change-the-data-retention-period)
* [Azure Monitor pricing](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#change-the-data-retention-period)

## How can I protect myself from unexpected large data ingestion?

To protect yourself from large unexpected data volumes and costs, you can configure a [daily cap](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#manage-your-maximum-daily-data-volume) to limit the daily ingestion for your workspace. Use care with this as your goal should not be to hit the daily limit because when the daily cap is met you lose data for the remainder of the day. As a result, your ability to observe and receive alerts when the health conditions of resources supporting IT services are impacted. The daily cap is intended to be used as a way to manage the unexpected increase in data volume from your managed resources and stay within your limit, or when you want to limit unplanned charges for your workspace.
To configure a limit to manage the volume of data that Log Analytics workspace will ingest per day, select **Usage and estimated costs** from the left pane in your workspace. On the **Usage and estimated costs** page for the selected workspace, click **Daily Cap** from the top of the page. Click the daily cap **ON** to enable it, and then set the data volume limit in GB/day. Note that security data types are not affected by the daily cap.
It is highly recommended to [configure an alert](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#alert-when-daily-cap-reached) so you know when the daily cap has been met.

## **Recommended Documents**
* [Setting a daily cap](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#manage-your-maximum-daily-data-volume)
* {Alert when the daily cap is reached](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#alert-when-daily-cap-reached)

## Why data is not flowing into my workspace

There are several reasons which may prevent data from being collected:

1. The Daily Cap you configured on your workspace was reached. You can either wait until the end of the 24 hour period for collection to resume, or [raise the Daily Cap setting](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#set-the-daily-cap).  To check the data collection status of your workspace from a , run the query:
`Operation | where OperationCategory == 'Data Collection Status'`. When data collection stops, the OperationStatus is **Warning**. When data collection starts, the OperationStatus is **Succeeded**. 
2. Your workspace has hit the [Data Ingestion Volume Rate](https://docs.microsoft.com/azure/azure-monitor/service-limits#log-analytics-workspaces). The default ingestion volume rate limit for data sent from Azure resources using diagnostic settings is approximately 6 GB/min per workspace. This is an approximate value since the actual size can vary between data types depending on the log length and its compression ratio. This limit does not apply to data that is sent from agents or Data Collector API. If you send data at a higher rate to a single workspace, some data is dropped, and an event is sent to the Operation table in your workspace every 6 hours while the threshold continues to be exceeded. If your ingestion volume continues to exceed the rate limit or you are expecting to reach it sometime soon, you can request an increase to your workspace by sending an email to LAIngestionRate@microsoft.com or opening a support request. The event to look for that indicates a data ingestion rate limit can be found by the query `Operation | where OperationCategory == "Ingestion" | where Detail startswith "The rate of data crossed the threshold"`.
3. If your workspace is in the legacy Free pricing tier, the workspace has a 500 MB/day daily cap.  You can either wait until the end of the 24 hour period for collection to resume, or change to the [Pay-As-You-Go pricing tier](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#changing-pricing-tier).
4. Azure subscription is in a suspended state due to your free trial ending, your Azure pass expiring or your monthly spending limit reached (for example on an MSDN or Visual Studio subscription). Depending on your situation, you can convert to a paid subscription, remove limit, or wait until limit resets. 

## **Recommended Documents**
* [Troubleshooting Log Analytics data collection](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#troubleshooting-why-log-analytics-is-no-longer-collecting-data)
* [Changing pricing tiers](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#changing-pricing-tier)
* [Managing your daily cap](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#set-the-daily-cap)
* [Log Analytics data ingestion volume rate](https://docs.microsoft.com/azure/azure-monitor/service-limits#log-analytics-workspaces)