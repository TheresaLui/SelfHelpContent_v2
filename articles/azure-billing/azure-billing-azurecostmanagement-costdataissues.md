<properties
	pageTitle="Cost Management - cost data issues"
	description="Cost Management - cost data issues"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32615284"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="9af7896e-f094-4405-8449-c79778dcf15b1"
	ownershipId="ASMS_Billing"
/>

# Cost Management - cost data issues

**How do I see the cost of each resource I’m using?**<br>
Cost analysis offers 4 built-in views to serve as a starting point for you to analyze costs. Open the view menu (between the scope and date pills) to reveal a list of all saved, shared, and built-in views.  Use the **Cost by resource** see costs broken down by each resource, sorted from most to least expensive within the date range (defaults to the current billing period). To see the individual meters for a specific resource, apply a resource filter and group by meter.<br>

**Tags I have set on resources are missing from Cost Management, can you explain why?**<br> 
Most taggable Azure services, emit tags to the Cost Management platform. However, a few services are yet to complete this work.  The following services don’t emit tags yet to the Cost Management platform:
* Azure Networking - VPN Gateway
* Azure ExpressRoute
* Azure Eventgrid
* Azure Firewall
* Azure Databricks
* Notification Hub
* Azure Subscriptions (Tag at sub level)
* Azure Compute | Disk Resource Provider (RP)
* Azure DataFactory
* Azure AppServices 
 
This is work in progress and we will update this list if any change occurs.<br>

## **Recommended Documents**

* [Costs included and not included in Cost Management](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data#costs-included-in-cost-management)<br>
* [Data refresh schedule](https://docs.microsoft.com/azure/cost-management-billing/costs/understand-cost-mgt-data#rated-usage-data-refresh-schedule)><br>
* [Usage data update frequency](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data#usage-data-update-frequency-varies)<br>
* [How to validate cost by analyzing usage](https://docs.microsoft.com/azure/billing/billing-understand-your-bill)<br>
* [Customize cost views](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis#customize-cost-views)<br>
* [View costs for a specific tag](https://docs.microsoft.com/azure/cost-management/cost-analysis-common-uses#view-costs-for-a-specific-tag)<br>
* [Use policy to enforce tag inheritance from RG to the resources in it](https://docs.microsoft.com/azure/governance/policy/tutorials/govern-tags)<br>
* [Cost Management best practices](https://docs.microsoft.com/azure/cost-management/cost-mgt-best-practices)<br>
* [What is Azure Cost Management?](https://docs.microsoft.com/azure/cost-management-billing/cost-management-billing-overview)<br>
