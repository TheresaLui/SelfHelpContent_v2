<properties 
    pageTitle="Where's my data (Latency)?"
    description="Where's my data (Latency)?"
    service="microsoft.insights"
    resource="components"
    articleId="insights-datalatency-mooncake"
    authors="debugthings"
    ms.author="jamdavi"
    displayOrder="6"
    selfHelpType="resource"
    productPesIds=""
    supportTopicIds=""
    cloudEnvironments="MoonCake"
	ownershipId="ASEP_ContentService_Placeholder"
/>
 
# Data latency

## **Recommended Steps**

Latency is expected in a highly distributed system. It is best to wait to see if the latency is persistent for more than two hours before attempting to open a ticket, as most latency issues are transient. To evaluate the actual amount of latency you can use the [ingestion_time()](https://docs.microsoft.com/azure/kusto/query/ingestiontimefunction) function. Here is an example query to investigate average latency per hour by data type:

1. Verify the version of the SDK you are using is up to date or a [supported version](https://github.com/Microsoft/ApplicationInsights-Home#officially-supported-sdks)  
2. Check the [Service Blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog) for any service outages
3. Execute a comparable query in Analytics and compare it to the other screens, as it's possible the data is not returned only for the impacted window
4. Verify the actual ingestion time compared to the timestamp using the query below

```
union *
| where timestamp > ago(24h)
| extend latency = ingestion_time() - timestamp
| summarize avg(latency) by itemType, bin(timestamp, 1h)
```

**Note**: We no longer have a data latency SLA. Please review our [current SLA](https://www.azure.cn/support/sla/monitor).


## **Recommended Documents**

* [Application Insights SLA](https://www.azure.cn/support/sla/monitor)
* [Checking Ingestion Time](https://docs.azure.cn/azure-monitor/platform/data-ingestion-time#checking-ingestion-time)
* [Service Blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)