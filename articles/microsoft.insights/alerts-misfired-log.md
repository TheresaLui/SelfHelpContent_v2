<properties
    pageTitle="My log search alert fired when it shouldn't have"
    description="My log search alert fired when it shouldn't have"
    infoBubbleText=""
    service="microsoft.insights"
    resource="scheduledqueryrules"
    authors="yalavi, yagil"
    ms.author="yalavi, yagil"
    displayOrder="8"
    articleId="alerts-misfired-log"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32612427, 32739783"
    resourceTags=""
    productPesIds="15454, 15725"
   cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_LogSearchAlerts"
/>

# My log search alert fired when it shouldn't have

[Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log) run your queries against the data in your [Log Analytics](https://docs.microsoft.com/azure/azure-monitor/log-query/log-query-overview) workspace or [Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview?toc=/azure/azure-monitor/toc.json) component.

## **Recommended Steps**

If you believe your log alert shouldn't have triggered but it did, the following steps may help resolve the issue.

1. Review the log alert rule to verify that the query run by the alert service is same as what you want:
    * Alerting service appends a ```| count``` for **Number of results** rules to compare the number of results for your query against the threshold
    * You can check the exact query used by the alerting service by [viewing the condition of your alert rule](https://docs.microsoft.com/azure/azure-monitor/platform/alert-log-troubleshoot#alert-query-output-misunderstood)
    * To resolve the issue, modify your alert rule query in log analytics portal, so that what alerting service runs matches what you want
    * You can use examples to understand what you can discover or [get started on writing queries](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal). Also, [learn how to create optimized alert queries](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-query).

2. Alert rule might have triggered based on partial data or no data being present:
    * As Azure Log Analytics is a high scale data service that serves thousands of customers  sending terabytes of data each month, it is sometimes susceptible to a varying time delay for data ingestion. For more information, see [Data ingestion time in Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time).
    * If the data queried by the alert rule is not yet fully ingested into Log Analytics, the alert rule might evaluate the condition as met because of which you might have received false alerts
    * If you are seeing this issue frequently, we recommend you to consider increasing the **period** used in your alert rule to reduce false alerts

## **Recommended Documents**

* [View/edit log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)
* [Troubleshoot log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alert-log-troubleshoot)
* [Understanding how log alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log)
