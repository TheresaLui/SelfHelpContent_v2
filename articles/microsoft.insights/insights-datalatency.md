<properties 
    pageTitle="Where's my data (Latency)?"
    description="Where's my data (Latency)?"
    service="microsoft.insights"
    resource="components"
    articleId="insights_datalatency"
    authors="jamdavi"
    ms.author="jamdavi"
    displayOrder="999"
    selfHelpType="resource"
    productPesIds="15693"
    supportTopicIds="32546624"
    cloudEnvironments="public"
/>
 
# Data latency

## **Recommended Steps**

Latency is expected in a highly distributed system. It is best to wait to see if the latency is persistent for more than two hours before attempting to open a ticket, as most latency issues are transient. To evaluate the actual amount of latency you can use the [ingestion_time()](https://docs.microsoft.com/en-us/azure/kusto/query/ingestiontimefunction) function. Here is an example query to investigate average latency per hour by data type. Please note, we no longer have a data latency SLA, please review our [current SLA](https://azure.microsoft.com/en-us/support/legal/sla/application-insights/v1_2/).<br>

1. Verify the version of the SDK you are using is up to date or a [supported version](https://github.com/Microsoft/ApplicationInsights-Home#officially-supported-sdks)  
2. Check the [Service Blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog) for any service outages
3. Execute a comparable query in Analytics and compare it to the other screens, as it's possible the data is not returned only for the impacted window
4. Verify the actual ingestion time compared to the timestamp using the query below

<br>
```
union *
| where timestamp > ago(24h)
| extend latency = ingestion_time() - timestamp
| summarize avg(latency) by itemType, bin(timestamp, 1h)
```

## **Recommended Documents**

* [Application Insights SLA](https://azure.microsoft.com/en-us/support/legal/sla/application-insights/v1_2/)<br>
* [Checking Ingestion Time](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-ingestion-time#checking-ingestion-time)<br>
* [Service Blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)<br>