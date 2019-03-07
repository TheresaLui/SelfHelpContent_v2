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

Data latency is an unfortunate part of a widely distributed collection system such as Application Insights and Azure Monitor. The **best case scenario** for data latency is usually limited to under 15 minutes. However there are many, many factors that can contribute to this and can lead to increased and unpredictable times. To evaluate the actual amount of latency you can use the [ingestion_time()](https://docs.microsoft.com/en-us/azure/kusto/query/ingestiontimefunction) function. Here is an example query to investigate average latency per hour by data type. Please note, we no longer have a data latency SLA, please review our [current SLA](https://azure.microsoft.com/en-us/support/legal/sla/application-insights/v1_2/).<br>

  1. Execute the query below
  2. Check the [Service Blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog) for a correlated incident
  3. If the query indicates that the period of latency is greater than one hour for an extended period of time (four or more hours) contact support.

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