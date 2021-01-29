<properties
    pageTitle="My log search alert didn't fire when it should have"
    description="My log search alert didn't fire when it should have"
    infoBubbleText=""
    service="microsoft.insights"
    resource="scheduledqueryrules"
    authors="yalavi, yagil"
    ms.author="yalavi, yagil"
    displayOrder="7"
    articleId="alerts-notfired-log"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32612428,32739784"
    resourceTags=""
    productPesIds="15454, 15725"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_LogSearchAlerts"
/>

# My log search alert didn't fire when it should have

[Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log) run your queries against the data in your [Log Analytics](https://docs.microsoft.com/azure/azure-monitor/log-query/log-query-overview) workspace or [Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-overview?toc=/azure/azure-monitor/toc.json) component and check if a predetermined threshold is met.

## **Recommended Steps**

If you believe your log alert should have triggered but it didn't, the following steps might help resolve the issue.

1. Review that the **period** field, which is set in the alert rule, is smaller than what is used in your query:
    * Log alerts are evaluated only based on data from the **period** specified in the alert rule
    * If this period is smaller than what you defined in your query (through an ago function), this might result in condition not matching and hence alert not triggering
    * [See an example to understand this issue](https://docs.microsoft.com/azure/azure-monitor/platform/alert-log-troubleshoot#incorrect-time-period-configured). You can resolve this issue by increasing the **period** set in your alert rule to match your query.

1. Review if the **Suppress Alerts** option is set for your rule:
    * If the suppress option is set, even if the condition is met, log alerts are suppressed
    * [Unselect the **Suppress Alerts** option to resolve this](https://docs.microsoft.com/azure/azure-monitor/platform/alert-log-troubleshoot#suppress-alerts-option-is-set)

1. If you are using a metric measurement type of alert with consecutive breaches condition, review if the query is set correctly:
    * Metric measurement alerts are a subtype of log alerts which need a more restricted query syntax
    * [See an example of an issue with metric measurement query and steps to resolve them](https://docs.microsoft.com/azure/azure-monitor/platform/alert-log-troubleshoot#metric-measurement-alert-rule-is-incorrect)

1. Run the query from your alert rule to check if the condition is met:
    * As Azure Log Analytics is a high scale data service that serves thousands of customers sending terabytes of data each month, it is sometimes susceptible to a varying time delay for data ingestion. For more information, see [Data ingestion time in Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time).
    * If the data queried by the alert rule is not yet fully ingested into Log Analytics, the alert rule might evaluate the condition as not met, because of which alert was not triggered
    * To avoid missed alerts, log alerts are retried with an exponential wait time. In such cases, you might receive alerts with a delay.

1. If the query doesn't work as expected, edit it from log analytics:

    * Select **View result of query in Azure Monitor - Logs** in the condition pane.
    * Query the log data that can indicate the issue. You can use examples to understand what you can discover or [get started on writing queries](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal). Also, [learn how to create optimized alert queries](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-query).

## **Recommended Documents**

* [How to view/edit log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)
* [How to troubleshoot log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alert-log-troubleshoot)
* [Understand how log alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log)
