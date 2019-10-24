<properties
	articleId="query-costanalysis-nulls"
	articleTags="costanalysis,views"
	pageTitle="Why am I seeing not applicable, unassigned, or others?"
	description="Not applicable and nulls"
	displayOrder="3"
	authors="flanakin"
	ms.author="micflan"
	selfHelpType="resource"
	service="microsoft.costmanagement"
	resource="query"
	resourceTags=""
	productPesIds="15659"
	supportTopicIds="32615286"
	cloudEnvironments="public,fairfax"
/>

# Why am I seeing "not applicable", "unassigned", or "others"?

"Not applicable" is shown when a value is empty. Here are a few reasons you might see "not applicable":

1. Tenant resources, which aren’t deployed within a subscription, will not have a resource group. This is expected. To validate this, download the data and review the ResourceId column.
2. Classic resources do not have a resource group. If you see a non-classic resource without a resource group, please contact support.
3. Purchases do not have a subscription, resource group, or resource. All of these values will show "not applicable".  To validate that this amount is from a purchase, switch to the **Invoice details** view and look at for a charge type of "purchase".

You may see an "unassigned" location for services which are not configured with a specific location. They may be global services, as an example.

"Others" is used in 2 contexts. A lowercase "others" resource group represents a missing or empty resource group. These are typically for classic resources. If you see "Others" as the last item in a chart that is grouped by a specific property, it represents all the remaining groups that aren't shown. Switch to the table view and set granularity to **None** to view all groups.

## **Recommended Documents**

* [Explore and analyze costs with cost analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)
* [Query API for rich reporting](https://docs.microsoft.com/rest/api/cost-management/query)
* [UsageDetails API for all cost and usage data](https://docs.microsoft.com/rest/api/consumption/usagedetails/list)
* [Understanding and working with scopes](https://docs.microsoft.com/azure/cost-management/understand-work-scopes)
* [Understanding cost and usage data](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data)
