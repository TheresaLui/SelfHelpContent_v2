<properties
	pageTitle="Unexpected cost in Cost analysis or Power BI"
	description="Unexpected cost in Cost analysis or Power BI"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615286"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="6365bccc-8864-4f10-a133-1acc5fb026b9"
	ownershipId="ASMS_Billing"
/>

# Unexpected cost in Cost analysis or Power BI

**Why am I seeing 'not applicable', 'unassigned', or 'others'?**<br>
'Not applicable' is used when a value is empty. Here are a few reasons you might see 'not applicable':<br>
Tenant resources, which aren’t deployed within a subscription, will not have a resource group. This is expected. To validate this, download the data and review the ResourceId column.<br>
Classic resources are not tracked with resource group. If you see a non-classic resource without a resource group, please contact support.<br>
Purchases do not have a subscription, resource group, or resource assigned. All of these values will show 'not applicable'. To validate that this amount is from a purchase, group by charge type.<br>
 
You may see an 'unassigned' location for services which are not configured with a specific location. They may be global services, as an example.<br>
 
'Others' is used in 2 contexts. A lowercase 'others' resource group represents a missing or empty resource group. These can be similar cases to 'not applicable' handling. If you see 'Others' as the last item in a chart that is grouped by a specific property, it represents all the remaining grouping segments that can’t be shown. Switch to the table view and set granularity to None to view all groupings.<br>

**Why am I seeing no cost (e.g. $0)?**<br>
If you see $0 (in your appropriate currency), consider the following:
* **Do you have any reservations?**<br>
Reservations are prepaid commitments to use a specific amount of Azure resources. All usage within that commitment will be $0. Filter down to the $0 resource, then group by reservation to see if a reservation was applied. If you see 'Not applicable' for the reservation, then one was not applied. Alternatively, use the 'Actual cost' KPI to switch to amortized cost, which will show the reservation cost broken down and allocated to each resource using the benefit.<br>

* **Did you get a refund?**<br>
By default, cost analysis aggregates all costs. If there’s a refund, you may see the sum of the purchase as well as the refund, which could be $0. To identify refunds, group by charge type and switch to a stacked column chart.<br>

* **Have you changed your indirect EA partner/reseller?**<br>
When an indirect EA partner changes within the middle of a billing term, access to costs will be disabled for the remainder of that billing term.<br>

## **Recommended Documents**

* [Costs included in Cost Management](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data#costs-included-in-cost-management)<br>
* [Data Refresh Schedules](https://docs.microsoft.com/azure/cost-management-billing/costs/understand-cost-mgt-data#rated-usage-data-refresh-schedule)<br>
* [Scopes in Cost Management](https://docs.microsoft.com/azure/cost-management/understand-work-scopes#scopes)<br>
* [Historical data in Cost Management](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data#historical-data-might-not-match-invoice)<br>
* [Cost Analysis and Invoice Reconciliation](https://azure.microsoft.com/blog/azure-cost-management-updates-september-2019/#invoices)<br>
* [How to validate cost by analyzing usage](https://docs.microsoft.com/azure/billing/billing-understand-your-bill)<br>
* [Connect to Azure Cost Management in Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-azure-cost-management)<br>
* [Cost Management best practices](https://docs.microsoft.com/azure/cost-management-billing/cost-management-billing-overview)<br>
* [What is Azure Cost Management?](https://docs.microsoft.com/azure/cost-management-billing/cost-management-billing-overview)<br>
