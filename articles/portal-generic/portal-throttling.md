<properties
    pageTitle="Azure Portal - Resource Manager Throttling"
    description="Azure Portal - Resource Manager Throttling"
    service="microsoft.portal"
    resource=""
    authors="rthorn17"
    ms.author="rithorn"
    displayorder=""
    selfHelpType="generic"
    articleId="portal-throttling"
    diagnosticScenario=""
    supportTopicIds="32637531"
    productPesIds="15739"
    cloudEnvironments="public, Fairfax, usnat, ussec, blackforest, mooncake"
	ownershipId="Compute_AzurePortal"
/>

# Resource Manager Throttling Help

For each Azure subscription and tenant, Resource Manager allows up to 12,000 read requests per hour and 1,200 write requests per hour. These limits are scoped to the security principal (user or application) making the requests and the subscription ID or tenant ID. If your requests come from more than one security principal, your limit across the subscription or tenant is greater than 12,000 and 1,200 per hour.

When you reach the limit, you will receive the **HTTP status code 429 Too many requests** response.

**Note**: Resource Graph sets its own limit and reset rate. For more information, see [Throttle in Azure Resource Graph](https://docs.microsoft.com/azure/governance/resource-graph/overview#throttling).

## **Recommended Steps**

* You can determine the number of remaining requests by examining response headers
* See [Resource Manager Throttling- Remaining Requests](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits#remaining-requests) for details on how to view your remaining requests using headers via C#, PowerShell, CLI, or API

## **Recommended Documents**

- For a complete PowerShell example, see [Check Resource Manager Limits for a Subscription](https://github.com/Microsoft/csa-misc-utils/tree/master/psh-GetArmLimitsViaAPI)
- For more information about limits and quotas, see [Azure subscription and service limits, quotas, and constraints](https://docs.microsoft.com/azure/azure-subscription-service-limits)
- To learn about handling asynchronous REST requests, see [Track asynchronous Azure operations](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-async-operations)
