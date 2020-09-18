<properties
    pageTitle="Metric API calls are being throttled"
    description="How to troubleshoot Metric API calls are being Throttled"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="2"
    articleId="metrics-api-calls-throttled"
    selfHelpType="generic"
    supportTopicIds="32684756"
    productPesIds="16250"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- metrics-api-calls-throttled -->

The metrics API is hosted behind the [Azure Resource Manager APIs](https://docs.microsoft.com/azure/azure-resource-manager). As a result, the metrics API is subject to the throttling limits as dictated by Azure Resource Manager. If you are calling the metric API very frequently, or are querying for metrics for many resources, you may run the risk of being throttled. Unfortunately, these throttling limits cannot be configured or raised on a per customer or subscription basis. The following diagram shows how throttling is applied as a request goes from the user to Azure Resource Manager and the resource provider:

![request throttling](https://docs.microsoft.com/azure/azure-resource-manager/media/resource-manager-request-limits/request-throttling.svg)

## **Recommended Steps**

1. Review [Azure Resource Manager’s throttling limits](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits)
1. Consider increasing your polling interval on the Metrics API to reduce the number of API calls you are generating per hour. For example, instead of querying metrics every minute, query every 5 minutes.
1. Build back-off capabilities into your querying by monitoring the [remaining requests in your API calls](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits)

## **Recommended Documents**

* [Azure Resource Manager Limits](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits)
* [Azure Resource Manager Documentation](https://docs.microsoft.com/azure/azure-resource-manager/)
