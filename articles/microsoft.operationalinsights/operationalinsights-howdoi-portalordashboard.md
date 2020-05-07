
<properties
pageTitle="Portal or dashboard not loading or throwing error"
description="Portal or dashboard not loading or throwing error"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="28d25b96-fca1-47f8-94e6-8bf406b283e4"
symptomID=""
infoBubbleText=""
authors="yossiy"
ms.author="yossiy"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612433"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, Blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Portal or dashboard not loading or throwing error

## **Recommended Steps**

Azure dashboard’s time picker restricts the time span for the parts in the dashboard. If you want to decouple the time span for particular Analytics parts on the dashboard, follow these steps:

1. Click the filter icon, located on the top left corner of Analytics parts
2. Select *Override the dashboard time settings at the tile level*
3. Set the desired *Timespan*<br>

Error messages:

* **oops… looks like we couldn’t get the data**: Workspace summary page may generate this error when reaching a query concurrency limit – it can happen normally when there are multiple tiles on the page. The limit is placed to isolate and protect customers in multitenancy platform.
* **No data**: Indicates that no record matched the query criteria
* **Error retrieving data**: The visualization part failed to receive results from the query engine. Verify the service status by clicking *Resource health* on Azure left navigation menu and [Azure Monitor Status](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog).

## **Recommended Documents**

* [Azure Monitor Status](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)
* [Azure status](https://azure.microsoft.com/status/)<br>
