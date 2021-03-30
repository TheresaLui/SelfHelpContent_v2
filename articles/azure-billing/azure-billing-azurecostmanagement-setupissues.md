<properties
  pagetitle="Azure Cost Management - Cost data is inconsistent or lagging&#xD;"
  service="azure-billing"
  resource="billing"
  ms.author="prdasneo,shasulin"
  selfhelptype="Generic"
  supporttopicids="32615287"
  resourcetags=""
  productpesids="15659"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="dded9c4c-4ba6-4a15-a000-af6e9017e48b"
  ownershipid="ASMS_Billing" />
# Azure Cost Management - Cost data is inconsistent or lagging

Cost and usage data is typically available in Cost Management + Billing in the Azure portal and supporting APIs within 8-24 hours. <br>

Keep the following points in mind as you review costs: <br>

- Each Azure service (such as Storage, Compute, and SQL) emits usage at different intervals. You might see data for some services sooner than others. <br>
- Estimated charges for the current billing period are updated 6 times per day. <br>
- Estimated charges for the current billing period can change as you incur more usage. <br>
- Each update is cumulative and includes all the line items and information from the previous update. <br>
- Azure finalizes or closes the current billing period up to 72 hours (three calendar days) after the billing period ends. 

<br>
The following examples illustrate how billing periods can end: <br>

- Enterprise Agreement (EA) subscriptions – If the billing month ends on March 31, estimated charges are updated up to 72 hours later. In this example, the estimated charges would be updated by midnight (UTC) on April 4. <b>
- Pay-as-you-go subscriptions – If the billing month ends on May 15, then the estimated charges might get updated up to 72 hours later. In this example, the estimated charges would be updated by midnight (UTC) on May 19. <br>
After cost and usage data becomes available in Cost Management + Billing, this data will be retained for at least 7 years.


## **Recommended Documents**

* [Data refresh schedules](https://docs.microsoft.com/azure/cost-management-billing/costs/understand-cost-mgt-data#rated-usage-data-refresh-schedule)<br>
* [Costs included in Cost Management](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data#costs-included-in-cost-management)<br>
* [Historical data in Cost Management](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data#historical-data-might-not-match-invoice)<br>
* [Usage data update frequency](https://docs.microsoft.com/azure/cost-management/understand-cost-mgt-data#usage-data-update-frequency-varies)<br>
* [Make the most out of Azure Cost Management](https://docs.microsoft.com/azure/cost-management/cost-mgt-best-practices)<br>
* [Azure Cost Management - Pricing](https://azure.microsoft.com/pricing/details/cost-management/)<br>
* [Explore and analyze costs with Cost analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Analyze your costs and spending](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
