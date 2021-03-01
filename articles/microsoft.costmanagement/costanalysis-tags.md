<properties
  pagetitle="Tags I have set on resources are missing from Cost Management, can you explain why?&#xD;"
  description="Tags on resource"
  service="microsoft.costmanagement"
  resource="costanalysis"
  ms.author="prdasneo,shasulin"
  selfhelptype="Resource"
  supporttopicids="32615286"
  resourcetags=""
  productpesids="15659"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="costanalysis-tags"
  ownershipid="ASMS_Billing" />
# Tags I have set on resources are missing from Cost Management, can you explain why?

Most taggable Azure services, emit tags to the Cost Management platform. However, a few services are yet to complete this work <br>  
 
The following services don’t emit tags yet to the Cost Management platform:

* Azure Active Directory Domain Services
* Azure Bastion
* Azure Event Grid
* Azure Firewall
* Azure NetApp Files
* Azure SQL Managed Instance (Databases)
* Azure Storage | Advanced Threat Protection
* Azure Subscriptions (Tag at sub level
* Notification Hub
* Virtual WAN

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