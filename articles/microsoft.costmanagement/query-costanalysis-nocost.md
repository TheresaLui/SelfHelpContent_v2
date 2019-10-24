<properties
	articleId="query-costanalysis-nocost"
	articleTags="data"
	pageTitle="Why am I seeing no cost (e.g. $0)?"
	description="No cost"
	displayOrder="4"
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

# Why am I seeing no cost (e.g. $0)?

## **Recommended Steps**

If you see $0 (in your appropriate currency), consider the following:

**Do you have any reservations?**

* Reservations are prepaid commitments to use a specific amount of Azure resources
* All usage within that commitment will be $0
* Filter down to the $0 resource, then group by reservation to see if a reservation was applied
* If you see "Not applicable" for the reservation, then one was not applied
* Alternatively, use the "Actual cost" KPI at the top-right, above the chart, to switch to "Amortized cost", which will show the reservation cost broken down and allocated to each resource using the benefit
* Amortized reservation costs will be lower the month of the reservation purchase and higher if the purchase was in a previous month

**Did you get a refund?**

* By default, cost analysis aggregates all costs
* If there's a refund, you may see the sum of the purchase as well as the refund, which could be $0 or even a negative number
* To identify refunds, switch to the **Invoice details** view

**Have you changed your indirect EA partner?**

* When an indirect EA partner changes within the middle of a billing term, access to costs will be disabled for the remainder of that billing term. This will resolve itself at the start of the next billing term.

## **Recommended Documents**

* [Explore and analyze costs with cost analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)
* [Query API for rich reporting](https://docs.microsoft.com/rest/api/cost-management/query)
* [UsageDetails API for all cost and usage data](https://docs.microsoft.com/rest/api/consumption/usagedetails/list)
* [Understanding and working with scopes](https://docs.microsoft.com/azure/cost-management/understand-work-scopes)
* [Understanding cost and usage data](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data)
