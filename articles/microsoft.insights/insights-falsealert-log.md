<properties
	pageTitle="My log search alert fired when it shouldn't have"
	description="My log search alert fired when it shouldn't have"
	infoBubbleText=""
	service="microsoft.insights"
	resource="scheduledqueryrules"
	authors="snehithm, msvijayn"
	authoralias="snmuvva, vinagara"
	displayOrder="8"
	articleId="falsealert-log"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629643, 32612427"
	resourceTags=""
	productPesIds="15454, 15725"​
	cloudEnvironments="public, fairfax"
/>

# My log search alert fired when it shouldn't have

[Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log) run the queries provided by you against the data in your [Log Analytics](https://docs.microsoft.com/azure/azure-monitor/log-query/log-query-overview) workspace or [Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview?toc=/azure/azure-monitor/toc.json) component and check if some threshold is met.

## **Recommended steps**

If you believe your log alert shouldn't have triggered but it did, the following steps might help resolve the issue.

1. Review the log alert rule to verify that the the query run by the alert service is same as what you want
    - Alerting service appends a ```| count``` for **Number of results** rules to compare the number of results for your query against the threshold
    - You can check the exact query used by the alerting service by [viewing the condition of your alert rule](https://docs.microsoft.com/azure/azure-monitor/platform/alert-log-troubleshoot#alert-query-output-misunderstood)
    - To resolve the issue, modify your alert rule query so that what alerting service runs matches what you want

2. Alert rule might have triggered based on partial data or no data being present
    - As Azure Log Analytics is a high scale data service that serves thousands of customers  sending terabytes of data each month, it is sometimes susceptible to a varying time delay for data ingestion. For more information, see [Data ingestion time in Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time)
    - If the data queried by the alert rule is not yet (fully) ingested into Log Analytics, the alert rule might evaluate the condition as met because of which you might have received false alerts
    - If you are seeing this issue frequently, we recommend you to consider increasing the **period** used in your alert rule to reduce false alerts

## **Recommended documents**

[How to view/edit log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)<br>
[How to troubleshoot log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alert-log-troubleshoot)<br>
[Understand how log alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log)<br>
