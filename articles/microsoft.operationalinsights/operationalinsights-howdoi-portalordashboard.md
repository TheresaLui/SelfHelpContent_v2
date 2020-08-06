
<properties
pageTitle="Portal or dashboard not loading or throwing error"
description="Portal or dashboard not loading or throwing error"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="28d25b96-fca1-47f8-94e6-8bf406b283e4"
symptomID=""
infoBubbleText=""
authors="roygal"
ms.author="rogal"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612433"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, Blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Portal or dashboard not loading or throwing error

### **Pinning A Log Analytics Visualization to an Azure Dashboard**

Log Analytics visualizations pinned to a dashboard have some specific considerations designed for an optimal dashboard experience, Please refer to the following items before submitting your support ticket:
### **1. I want to report a time scope larger than 30 days:** 
As dashboards may contain multiple visualizations from multiple queries, the time scope for a single pinned query is limited to 30 days.
	
This means that a single query may only run on a time span smaller or equal to 30 days.
This is done so we can ensure a reasonable load time for a dashboard. 

### **2. My query returns a large number of data values:**

Dashboards are a visually dense and complex artifacts. 
In order for us to reduce cognitive load when viewing a dashboard we optimize the visualizations, loading up to 25 different data values.
In the rare case where a visualization has more than 25 different data values, Log Analytics will optimize it, showing the 25 values with most data as discrete data values and grouping the remaining values under an other value.

###	**3. I want my dashboard to auto refresh:** 

Dashboards are refreshed upon load; this  means all queries related to a pinned Log Analytics visualizations in the dashboard are executed and the dashboard is refreshed once it loads.

### **4. Azure dashboard’s time picker restricts the time span for the parts in the dashboard:** 
If you want to decouple the time span for particular Analytics parts on the dashboard, follow these steps:
1. Click the filter icon, located on the top left corner of Analytics parts
2. Select *Override the dashboard time settings at the tile level*
3. Set the desired *Timespan*

### **5. Additional resources:**
Log Analytics offers a variety of additional ways to integrate and create dashboards: </br>
1.	[Create a Power BI dashboard](https://docs.microsoft.com/azure/azure-monitor/platform/powerbi) </br>
2.	[Create a Grafana dashboard](https://azure.microsoft.com/blog/azure-monitor-logs-in-grafana-now-in-public-preview/)


### **6. Common error messages:** <body> 
	
* **oops… looks like we couldn’t get the data**: Workspace summary page may generate this error when reaching a query concurrency limit – it can happen normally when there are multiple tiles on the page. The limit is placed to isolate and protect customers in multitenancy platform.
	
* **No data**: Indicates that no record matched the query criteria
	
* **Error retrieving data**: The visualization part failed to receive results from the query engine. Verify the service status by clicking *Resource health* on Azure left navigation menu and [Azure Monitor Status](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog).
</body>

## **Recommended Documents**

* [Azure Monitor Status](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)
* [Azure status](https://azure.microsoft.com/status/)<br>
