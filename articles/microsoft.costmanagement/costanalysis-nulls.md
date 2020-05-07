<properties
	articleId="costanalysis-nulls"
	articleTags="costanalysis,data"
	pageTitle="Why am I seeing not applicable, unassigned, $system, or others?"
	description="Not applicable and nulls"
	displayOrder="2"
	authors="flanakin"
	ms.author="micflan"
	selfHelpType="resource"
	service="microsoft.costmanagement"
	resource="costanalysis"
	resourceTags=""
	productPesIds="15659"
	supportTopicIds="32615286"
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="ASMS_Billing"
/>

# Why am I seeing not applicable, unassigned, $system, or others?

## **Recommended Steps**

"Not applicable" is shown when a value is empty. Here are a few reasons you might see "not applicable" or other unexpected values:

**Tenant or untracked resources**

Tenant resources aren’t deployed within a subscription. Untracked (or proxy) resources may be services enabled for an entire subscription, like Azure Security Center, or resources that aren't deployed to a resource group. In either case, these resources will not have a resource group and may show as either "Not applicable" or "$system". To validate this:

1. Open the view menu (between scope and date pills)
2. Switch to **Cost by resource**
3. Click the **Export** command at the top
4. In the Download section, select **Excel** or **CSV** and click **Download data**
5. If using Excel, switch to the **Data** tab
6. Review the **ResourceId** column

Tenant resources have a resource ID that starts with "/providers". Untracked resources have a resource ID that starts with "/subscriptions/{id}/providers" and do not include a resource group name.

**Reservation and Marketplace purchases**

Purchases do not have a subscription, resource group, or resource. Marketplace purchases do not have an associated meter or service. All of these values will show "not applicable" or "unassigned". To validate if an amount is from a purchase:

1. Open the view menu (between scope and date pills)
2. Switch to **Invoice details**
3. Type "purchase" (in English) in the filter box to only see purchases
4. Locate the amount in question and review the publisher type, charge type, and service/meter details

Azure purchases in Enterprise Agreement accounts are reservations. Microsoft Customer Agreement accounts may include other Azure purchases, like Support.

**Global services**

Services that are global or not deployed to a specific Azure region, like Marketplace offers, may have a location value of "not applicable" or "unassigned" (in English). This may be surfaced as a separate record from the actual resource, which does have a location.

**Others**

"Others" is used in 2 contexts. A lowercase "others" (in English) resource group represents a missing or empty resource group. These are typically for classic resources. If you see "Others" as the last item in a chart legend that is grouped by a specific property, it represents all the remaining groups that aren't shown. To see more than the top 9 groups:

1. Click the visualization picker above the chart on the right and select **Table**
2. Click the **Granularity** dropdown and select **None** to see the total value for the period (instead of daily or monthly data)

The table will be sorted from the highest cost to the lowest.

## **Recommended Documents**

* [Explore and analyze costs with cost analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)
* [Query API for rich reporting](https://docs.microsoft.com/rest/api/cost-management/query)
* [UsageDetails API for all cost and usage data](https://docs.microsoft.com/rest/api/consumption/usagedetails/list)
* [Understanding and working with scopes](https://docs.microsoft.com/azure/cost-management/understand-work-scopes)
* [Understanding cost and usage data](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data)
