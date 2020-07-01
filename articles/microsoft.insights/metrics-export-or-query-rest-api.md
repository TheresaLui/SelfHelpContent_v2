<properties
    pageTitle="Issue querying metrics using REST API"
    description="How to troubleshoot issues with querying metrics using REST API"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="2"
    articleId="metrics-export-or-query-rest-api"
    selfHelpType="generic"
    supportTopicIds="32684743"
    productPesIds="16250"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- metrics-export-or-query-rest-api -->

**NOTE:** If you need to query metrics programmatically without the context of the authenticated user, you need to create and use a service account as described in [How to: Use the portal to create an Azure AD application and service principal that can access resources](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal).

When you are making REST API calls for metrics, you may receive one the following error messages or indications of a problem: 
* "Authorization Failed" error message
* "This subscription is not registered with the Microsoft.Insights resource provider" error message
* Metric does not exist (the Bad Request response code is returned)
* No metrics data is returned
* Other issues with the REST API call that return the  Bad Request response code

## **Recommended Steps**

**Authentication Failed** error message

This error is returned when the user or the application querying for metrics on the resource does not have sufficient permissions to perform the "metrics read" action. In Azure, access to metrics is controlled by [role-based access control (RBAC)](https://docs.microsoft.com/azure/role-based-access-control/overview). The user or service account querying for metrics must be a member of [monitoring reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-reader), [monitoring contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-contributor), or [contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#contributor) to explore metrics for any resource.

1. Review how to [grant a user access to Azure resources using RBAC and the Azure portal](https://docs.microsoft.com/azure/role-based-access-control/quickstart-assign-role-user-portal)
1. Add user or application service principal account to the [monitoring reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-reader), [monitoring contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-contributor), or [contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#contributor) roles

**This subscription is not registered with the Microsoft.Insights resource provider** error message

To query for metrics using REST API it is necessary to register *Microsoft.Insights* resource provider for your subscription. In many cases, it is registered automatically (that is, after you configure an alert rule, customize diagnostic settings for any resource, or configure an autoscale rule). In other cases, you need to manually register the resource provider:

1. Navigate to the Azure Portal and open **Subscriptions** 
2. Under **Settings**, click on the **Resource providers** tab 
3. Search for the *Microsoft.Insights* resource provider and register it for your subscription

**Metric does not exist** (the Bad Request response code is returned)

When querying for metrics for a resource, it is important to note there are two name properties ("MetricName" and "MetricDisplayName") for each metric. The REST API query should be using the "MetricName" (and NOT the MetricDisplayName) property:

1. Navigate to the [list of supported metrics](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported) and ensure you are querying using the correct metric name
1. Alternatively, query for all metric definitions for a metric first, by using the [metric definitions api](https://docs.microsoft.com/rest/api/monitor/metricdefinitions/list)
1. If you are querying for a custom metric, ensure you have specified both, the correct metric namespace, and metric name in your query parameters. Review the [metric REST API](https://docs.microsoft.com/rest/api/monitor/metrics/list) to verify that you are setting these properties correctly. 

**No metrics data is returned**

There are times when the metrics API will return a response with no data at all. This can occur for a few reasons:

* You have specified an invalid time range, outside of the available metric retention window, or a time range greater than 30 days
* Some resources don’t constantly emit their metrics. For example, Azure will not collect metrics for stopped virtual machines. 
* Certain resources might emit their metrics only when some condition occurs. For example, a metric showing processing time of a transaction requires at least one transaction. If there were no transactions in the selected time range, the API response will contain no data.

When  metrics API call returns no data at all: 

1. Ensure the time range of your query is no larger than 30 days
1. Ensure you are not querying for metric data older than 93 days
1. Ensure your resource should have been emitting data during the given time range. Try expanding your time range to a time you expected data to be emitted and validate if you see data.
1. To confirm that the resource has any metric data, try plotting a metric chart for the same metric and resource by using [Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)

**Other issues with the REST API calls that return the Bad Request response code**

The metrics REST API has parameters for specifying the time range, dimension filters, aggregation types, and sort order. An incorrect value in any of these parameters will result in a "Bad Requests" response code. To learn about the expected format of each parameter, review the [Metric Definitions REST API specification](https://docs.microsoft.com/rest/api/monitor/metricdefinitions/list), [Metrics REST API specification](https://docs.microsoft.com/rest/api/monitor/metrics/list), and [Azure Monitoring REST API walkthrough](https://docs.microsoft.com/azure/azure-monitor/platform/rest-api-walkthrough).

## **Recommended Documents**

* [Azure role-based access control (RBAC)](https://docs.microsoft.com/azure/role-based-access-control/overview)
* [Monitoring roles](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security)
* [Registering Azure’s resource providers and types](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-supported-services) 
* [Metrics REST API walkthrough](https://docs.microsoft.com/azure/azure-monitor/platform/rest-api-walkthrough)
* [Metrics API reference](https://docs.microsoft.com/rest/api/monitor/)
