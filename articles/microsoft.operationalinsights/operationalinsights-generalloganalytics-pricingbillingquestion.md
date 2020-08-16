
<properties
pageTitle="Pricing or billing question"
description="Pricing or billing question"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="yossiy,dalek,shemers"
ms.author="yossiy,dalek,shemers"
displayorder="12"
selfHelpType="generic"
supportTopicIds="32612512"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
articleId="29181eef-5603-4200-8acf-ae7d5317aaa9"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Billing, data volume and retention


## How can I understand my workspace’s usage?<br>

The Log Analytics page 'Usage and estimated costs' has information on your estimated monthly costs based on the last 30 days of usage. Additionally, there is a chart of data volume ingested so you can see any trends and information on which solutions account for the most data volume. From your workspace, click 'Usage and estimated costs' on the left navigation pane to see information on your [estimated monthly costs](https://docs.microsoft.com/azure/azure-monitor/platform/data-usage)based on the last 30 days of usage. Additionally, there is a chart of data volume ingested so you can see any trends and information on which solutions account for the most data volume.

## **Recommended Documents**
* [Usage and estimated costs](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#understand-your-usage-and-estimate-costs)
* [Understanding the source of your workspace’s data ingestion](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#understanding-ingested-data-volume)
* [Log Analytics pricing model](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#pricing-model)

## How can I understand my workspace’s billed costs? <br>

To understand what you have actually been billed, Azure provides a great deal of useful functionality in the [Azure Cost Management + Billing](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis?toc=/azure/billing/TOC.json) hub. For instance, the 'Cost analysis' functionality enables you to view your spends for Azure resources. Adding a filter by resource type (to microsoft.operationalinsights/workspace for Log Analytics) will allow you to track your spend.
</br></br>
More understanding of your usage can be gained by [downloading your usage from the Azure portal](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date#download-usage-in-azure-portal). In the downloaded spreadsheet you can see usage per Azure resource (e.g. Log Analytics workspace) per day. In this Excel spreadsheet, usage from your Log Analytics workspaces can be found by first filtering on the 'Meter Category' column to show 'Insights and Analytics' (used by some of the legacy pricing tiers) and 'Log Analytics', and then adding a filter on the 'Instance ID' column which is 'contains workspace'. The usage is shown in the 'Consumed Quantity' column and the unit for each entry is shown in the 'Unit of Measure' column. More details are available to help you [understand your Microsoft Azure bill](https://docs.microsoft.com/azure/billing/billing-understand-your-bill).

## **Recommended Documents**
* [Azure Monitor pricing](https://azure.microsoft.com/pricing/details/monitor/)

## How can I select the best pricing tier for me?</br>
In the Azure portal, open **Usage and estimated costs** from your workspace where you'll see a list of each of the pricing tiers available to your workspace. Review the estimated costs if the workspace were in each of the pricing tiers based on the last 31 days of usage. This will guide you to the most cost-effective pricing tier. Note that if you own OMS Suite licenses, you should put your workspace into the Per Node pricing tier to leverage your licenses. [Learn more](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#changing-pricing-tier) about Log Analytics pricing tiers. 

## **Recommended Documents**
* [Changing pricing tiers](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#changing-pricing-tier)
* [Log Analytics pricing model](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#pricing-model)
* [Azure Monitor pricing](https://azure.microsoft.com/pricing/details/monitor/)


## How can I protect myself from unexpected large data ingestion?</br>
To protect yourself from large unexpected data volumes and costs, you can configure a [daily cap](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#manage-your-maximum-daily-data-volume) to limit the daily ingestion for your workspace. Use care with this as your goal should not be to hit the daily limit because when the daily cap is met you lose data for the remainder of the day. As a result, your ability to observe and receive alerts when the health conditions of resources supporting IT services are impacted. The daily cap is intended to be used as a way to manage the unexpected increase in data volume from your managed resources and stay within your limit, or when you want to limit unplanned charges for your workspace.</br></br>
To configure a limit to manage the volume of data that Log Analytics workspace will ingest per day, select **Usage and estimated costs** from the left pane in your workspace. On the **Usage and estimated costs** page for the selected workspace, click **Data volume management** from the top of the page. Click the daily cap **ON** to enable it, and then set the data volume limit in GB/day.</br></br>
It is highly recommended to [configure an alert](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#alert-when-daily-cap-reached) so you know when the daily cap has been met.

## **Recommended Documents**
* [Understanding the source of your workspace’s data ingestion](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#understanding-ingested-data-volume)
* [Log Analytics pricing model](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#pricing-model)
* [Azure Monitor pricing](https://azure.microsoft.com/pricing/details/monitor/)

## How can I configure my workspace’s data retention?</br>
To set the default retention for your workspace, from your workspace, select **Usage and estimated costs** from the left pane. On the **Usage and estimated costs** page, click **Data volume management** from the top of the page. On the pane, move the slider to increase or decrease the number of days and then click **OK**. If you are on the free tier, you will not be able to modify the data retention period and you need to upgrade to the paid tier in order to control this setting. Note that there are charges for additional retention. See details on the [Azure Monitor pricing page](https://azure.microsoft.com/pricing/details/monitor/). 

## **Recommended Documents**
* [Managing your workspace’s data retention](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#change-the-data-retention-period)
* [Azure Monitor pricing](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#change-the-data-retention-period)


## Data is not flowing into my workspace due to daily cap </br>

To check the data collection status of your workspace, run the query:</br>
```Operation | where OperationCategory == 'Data Collection Status'```</br>
When data collection stops, the OperationStatus is **Warning**. When data collection starts, the OperationStatus is **Succeeded**. </br></br>
There are three main reasons why this will show that data is not being collected:
1.	Daily Cap you configured on your workspace was reached. You can either wait until the end of the 24 hour period for collection to resume, or [raise the Daily Cap setting](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#set-the-daily-cap). 
2.	If your workspace is in the legacy Free pricing tier, the workspace has a 500 MB/day daily cap.  You can either wait until the end of the 24 hour period for collection to resume, or change to the [Pay-As-You-Go pricing tier](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#changing-pricing-tier).
3.	Azure subscription is in a suspended state due to your free trial ending, your Azure pass expiring or your monthly spending limit reached (for example on an MSDN or Visual Studio subscription). Depending on your situation, you can convert to a paid subscription, remove limit, or wait until limit resets. 

## **Recommended Documents**
* [Troubleshooting Log Analytics data collection](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#troubleshooting-why-log-analytics-is-no-longer-collecting-data)
* [Changing pricing tiers](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#troubleshooting-why-log-analytics-is-no-longer-collecting-data)
* [Managing your daily cap](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#troubleshooting-why-log-analytics-is-no-longer-collecting-data)
