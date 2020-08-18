<properties
    pageTitle="Difference between log-based and standard metrics in Application Insights"
    description="Difference between log-based and standard metrics in Application Insights"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="2"
    articleId="metrics-resourcespecific-appinsights-log-or-preagg"
    selfHelpType="generic"
    supportTopicIds="32684748,32730384"
    productPesIds="16250"
    cloudEnvironments="public,fairfax,mooncake,blackforest,usnat,ussec"
    ownershipId="AzureMonitoring_Essentials"
/>

# <-- metrics-resourcespecific-appinsights-log-or-preagg -->

Application Insights has two types of metrics: the metrics that are based on the captured events in logs are called *log-based metrics*, and *standard metrics* that are pre-aggregated during collection and stored in the Azure metrics repository. Each metric type brings a unique value in monitoring application health, diagnostics and analytics. The developers who are instrumenting their applications can decide which type of metric is best suited to a particular scenario, depending on the size of the application, expected volume of telemetry, and business requirements for metrics precision and alerting.

The **log-based metrics** behind the scene is an abstraction layer that translates each request for metric values into a Kusto query on top of raw events. See [the underlying queries for each Application Insights log-based metric](https://docs.microsoft.com/azure/azure-monitor/platform/app-insights-metrics). The log-based metrics have more dimensions and, therefore, have greater analytical value but the accuracy of log-based metrics may be impacted by the telemetry volume reduction techniques such as sampling, filtering, or data capping.

The **standard pre-aggregated metrics** provide faster query time and high precision (as they aren't impacted by sampling, filtering, or data-capping), which makes them a superior choice for alerting or dashboards. However, standard pre-aggregated metrics have fewer dimensions and may be more limited in the analytical scenarios.

## **Recommended Documents**

* [Log-based and pre-aggregated metrics in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/pre-aggregated-metrics-log-metrics)
* [Kusto queries for Application Insights log-based metric](https://docs.microsoft.com/azure/azure-monitor/platform/app-insights-metrics)
* [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)
* [Advanced features of Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts)
