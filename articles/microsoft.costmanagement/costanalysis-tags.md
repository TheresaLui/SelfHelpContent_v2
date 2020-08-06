<properties
	articleId="costanalysis-tags"
	articleTags="costanalysis,tags"
	pageTitle="Tags I have set on resources are missing from Cost Management, can you explain why?"
	description="Tags on resource"
	displayOrder="7"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="resource"
	service="microsoft.costmanagement"
	resource="costanalysis"
	resourceTags=""
	productPesIds="15659"
	supportTopicIds="32615286"
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="ASMS_Billing"
/>

# Tags I have set on resources are missing from Cost Management, can you explain why?

Most taggable Azure services, emit tags to the Cost Management platform. However, a few services are yet to complete this work <br>  
 
The following services don’t emit tags yet to the Cost Management platform:

* Azure Networking - VPN Gateway
* Azure ExpressRoute
* Azure Eventgrid
* Azure Firewall
* Azure Databricks
* Notification Hub
* Azure Subscriptions (Tag at sub level)
* Azure Compute | Disk Resource Provider (RP)
* Azure DataFactory
* Azure AppServices 
 
This is work in progress and we will update this list if any change occurs <br>


## **Recommended Documents**

* [Costs included and not included in Cost Management](https://docs.microsoft.com/azure/cost-management-billing/costs/understand-cost-mgt-data#costs-included-in-cost-management)
* [Data refresh schedule](https://docs.microsoft.com/azure/cost-management-billing/costs/understand-cost-mgt-data#rated-usage-data-refresh-schedule)
* [Usage data update frequency](https://docs.microsoft.com/azure/cost-management-billing/costs/understand-cost-mgt-data#usage-data-update-frequency-varies)
* [How to validate cost by analyzing usage](https://docs.microsoft.com/azure/cost-management-billing/understand/review-individual-bill)
* [Customize cost views](https://docs.microsoft.com/azure/cost-management-billing/costs/quick-acm-cost-analysis#customize-cost-views)
* [View costs for a specific tag](https://docs.microsoft.com/azure/cost-management-billing/costs/cost-analysis-common-uses#view-costs-for-a-specific-tag)
* [Use policy to enforce tag inheritance from RG to the resources in it](https://docs.microsoft.com/azure/governance/policy/tutorials/govern-tags)
* [Cost Management best practices](https://docs.microsoft.com/azure/cost-management-billing/costs/cost-mgt-best-practices)
* [What is Azure Cost Management?](https://docs.microsoft.com/azure/cost-management-billing/cost-management-billing-overview)
