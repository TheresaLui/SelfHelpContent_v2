<properties
    pageTitle="Autoscale didn't scale as expected or scaled when it shouldn't"
    description="Autoscale didn't scale as expected or scaled when it shouldn't"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="2"
    articleId="autoscale-action-behavior"
    selfHelpType="generic"
    supportTopicIds="32683737,32683738"
    productPesIds="15527"
    cloudEnvironments="public,fairfax,mooncake,blackforest,usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- autoscale-action-behavior -->

You can use *metrics*, *scale action logs*, and *scale condition evaluation logs* to investigate why the autoscale engine did (or did not) perform a scale action. The autoscale metrics are always on and can be seen in [Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started) at any time. The *scale actions* are logged into the **Activity Log** when scale actions occur. To view more detailed *scale evaluation logs*, you must first turn on the **Diagnostic Settings** for Autoscale and [send the logs to Log Analytics workspace](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#destinations).

## **Recommended Steps**

1. Navigate to [Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started) in Azure Portal
1. In the [resource picker](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started#create-your-first-metric-chart), apply filter to only display the **Autoscale settings** resource type. Then select the autoscale settings resource that you want to investigate
1. Use the following metrics to analyze operations of the autoscale engine:
    * **Observed Metric Value** - The value of the metric that autoscale engine evaluates by comparing it with the threshold to determine if scale action should occur. Since single autoscale setting can have multiple rules (and therefore multiple metric sources), you may need to [apply a filter](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#apply-filters-to-charts) on the *metric source* dimension
    * **Metric Threshold** - The threshold value used in autoscale condition evaluations. Because a single autoscale setting can have multiple rules (and therefore multiple metric sources), you may need to apply a filter on the *metric rule* dimension
    * **Observed Capacity** - The active number of instances of the target resource as seen by the Autoscale engine
    * **Scale Actions Initiated** - The number of scale-out and scale-in actions initiated by the autoscale engine. You can filter by the scale-out and scale-in actions
1. For additional information about diagnosing autoscale, use the [Troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)

## **Recommended Documents**

* [Overview of autoscale in Microsoft Azure Virtual Machines, Cloud Services, and Web Apps](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-overview)
* [Get started with autoscale in Azure](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-get-started)
* [Troubleshooting guide for Azure Monitor autoscale](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-troubleshoot)
