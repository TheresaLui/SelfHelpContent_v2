<properties
    pageTitle="Action or notification happened with delay"
    description="The action happen long time after the alert arrived to the portal"
    infoBubbleText=""
    service="microsoft.insights"
    resource="actiongroups"
    authors="yairgil"
	ms.author="yagil"
    displayOrder="1"
    articleId="alerts-notification-delay"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739761,32633012"
    resourceTags=""
    productPesIds="15454,15725"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# My log search alert fires with a delay

[Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log) run your queries against the data in your [Log Analytics](https://docs.microsoft.com/azure/azure-monitor/log-query/log-query-overview) workspace or [Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview?toc=/azure/azure-monitor/toc.json) component.

## **Recommended Steps**

If you believe your log alert is triggering with a delay, the following steps might help you understand and resolve issues.

Data ingestion time into Log Analytics or Application Insights might be impacting your alert rule:

* Azure Log Analytics and Application Insights are high scale data services that serves thousands of customers sending terabytes of data each month, and can sometimes be susceptible to a varying time delay for data ingestion. For more information, see [Data ingestion time in Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time).

* If the data queried by the alert rule is not yet (fully) ingested into Log Analytics or Application Insights, the alert rule might evaluate the condition as not met because of which alert was not triggered

* To avoid missed alerts in such cases, log alerts are retried several times with an exponential wait time

* When the condition is not met during the initial execution but on a retry, you might receive alerts with a delay

* If you need alerts with a lower latency, consider using [Metric alerts for Logs](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs) for alerting on Heartbeat, Perf, or Events tables

## **Recommended Documents**

* [How to view/edit log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)<br>
* [How to troubleshoot log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alert-log-troubleshoot)<br>
* [Understanding log alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log)<br>
