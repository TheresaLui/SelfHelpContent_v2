<properties
    pageTitle="Gernric Guidance for Throttling in Azure Resource Graph"
    description="This page provides guidance for throttling in Azure Resource Graph"
    service="microsoft.resourcegraph"
    resource="resources"
    authors="chiragg4u"
    ms.author="chgupta"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32636057"
    resourceTags=""
    productPesIds="16716"
    cloudEnvironments="public"
    articleId="4b243b0b-efa6-4a75-a500-8b6645a27c24"
/>

# Azure Resource Graph - Throttling Errors

This support request will be filed for "Azure Resource Graph" (ARG) service. Azure Resource Graph is exposed in:

* Azure Portal Search, "All Resources" view, and "Resource Graph Explorer". 
* Azure CLI with the following command "az graph query", 
* Azure Powershell with the following command "Search-AzGraph -Query", 
* API under Azure resource provider "Microsoft.ResourceGraph".

Throttling error with "Azure Resource Graph" service call usually occurs when the client is trying to utilize too many resources on the server side. Azure Resource Graph is designed for at scale queries but client need to optimize the queries to be able to use the full capabilities. 

## **Recommended Documents**

* [Understand throttling headers](https://docs.microsoft.com/azure/governance/resource-graph/concepts/guidance-for-throttled-requests#understand-throttling-headers)
* [Batching queries](https://docs.microsoft.com/azure/governance/resource-graph/concepts/guidance-for-throttled-requests#batching-queries)
* [Staggering queries](https://docs.microsoft.com/azure/governance/resource-graph/concepts/guidance-for-throttled-requests#staggering-queries)
* [Pagination](https://docs.microsoft.com/azure/governance/resource-graph/concepts/guidance-for-throttled-requests#pagination)

If the above information does not resolve the issue you are facing, then proceed to file the support request.