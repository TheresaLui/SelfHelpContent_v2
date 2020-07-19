<properties
    pageTitle="Generic Guidance for Throttling in Azure Resource Graph"
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
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="4b243b0b-efa6-4a75-a500-8b6645a27c24"
	ownershipId="compute_azureresourcegraph"
/>

# Azure Resource Graph - Throttling Errors

*If you're hitting issues regarding Microsoft Graph API, please create your support request under "Azure Active Directory App Integration and Development" service, and choose Graph API as your problem type.*

This support request will be created for "Azure Resource Graph" (ARG) service. Azure Resource Graph is exposed in the following ways:

* Azure Portal Search, "All Resources" view, and "Resource Graph Explorer" 
* Azure CLI with the command `az graph query`
* Azure Powershell with the command `Search-AzGraph -Query`
* API under Azure resource provider "Microsoft.ResourceGraph"

Throttling error with "Azure Resource Graph" service call usually occurs when the client is trying to utilize too many resources on the server side. Azure Resource Graph is designed for at scale queries but client need to optimize the queries to be able to use the full capabilities. 

## **Recommended Documents**

* [Understand throttling headers](https://docs.microsoft.com/azure/governance/resource-graph/concepts/guidance-for-throttled-requests#understand-throttling-headers)
* [Batching queries](https://docs.microsoft.com/azure/governance/resource-graph/concepts/guidance-for-throttled-requests#batching-queries)
* [Staggering queries](https://docs.microsoft.com/azure/governance/resource-graph/concepts/guidance-for-throttled-requests#staggering-queries)
* [Pagination](https://docs.microsoft.com/azure/governance/resource-graph/concepts/guidance-for-throttled-requests#pagination)

If the above information does not resolve the issue you are facing, then proceed to file the support request.
