<properties
	articleId="costanalysis-nocost"
	articleTags="data"
	pageTitle="Why am I seeing no cost (e.g. $0)?"
	description="No cost"
	displayOrder="3"
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

# Why am I seeing no cost (e.g. $0)?

## **Recommended Steps**

If you see $0 (in your appropriate currency), consider the following:

**Do you have any reservations?**

Reservations are prepaid commitments to use a specific amount of Azure resources. All usage within that commitment will be $0. To confirm reservation usage:

1. Filter down to the resource showing $0 cost
2. Group by **Reservation** to see if a reservation was applied – "Not applicable" means there is no reservation
3. If a reservation was applied, change the **Actual cost** KPI at the top right, above the chart, to **Amortized cost**

Amortized costs break reservation purchases down and allocate the purchase costs to the individual resources which used the reservation benefit. Amortized costs will be lower if a reservation was purchased during the selected period and higher if the reservation was purchased before the current period.

**Did you get a refund?**

Cost analysis aggregates all costs. If there's a refund, you may see the sum of the purchase as well as the refund, which could be $0 or even a negative number. In an accumulated chart, you may see cost increase, then decline (the refund), and increase again. In a column chart, you may see both positive and negative chart segments. To confirm refunds:

1. Open the view menu (between the scope and date pills)
2. Switch to the **Invoice details** view
3. Type "refund" into the filter box above the table to only see refunds

**Have you changed your indirect EA partner?**

When an indirect EA partner changes within the middle of a billing term, access to costs will be disabled for the remainder of that billing term. This will resolve itself at the start of the next billing term.

## **Recommended Documents**

* [Explore and analyze costs with cost analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)
* [Query API for rich reporting](https://docs.microsoft.com/rest/api/cost-management/query)
* [UsageDetails API for all cost and usage data](https://docs.microsoft.com/rest/api/consumption/usagedetails/list)
* [Understanding and working with scopes](https://docs.microsoft.com/azure/cost-management/understand-work-scopes)
* [Understanding cost and usage data](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data)
