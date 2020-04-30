<properties
	pageTitle="cost discrepancy or missing data"
	description="cost discrepancy or missing data"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615288"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="6182a7a3-a056-4149-b654-99ae60919c18"
	ownershipId="ASMS_Billing"
/>

# Cost Discrepancy or Missing Data

### **Discrepancy between Cloudyn and Azure billing data**

Discrepancy between Cloudyn data and Azure billing data is expected. This is because Cloudyn calculates costs for CSP customers by multiplying usage * rate. Cloudyn costs are an estimate of Azure costs (which often differ by 2-3% and may differ by up to 10% lower or 15% higher than the Partner Center for CSP customers). Taxes, currency rates, and round off also cause slight differences for CSP customers. Cloudyn usually shows slightly more usage data than Azure since Azure rounds down for billing purposes.

Some other reasons for the discrepancy:

* CSP billing cycle may start anywhere during the month. Cloudyn’s month is always from the 1st of the month until the last month day (inclusive).
* CSP closes the cost calculation at some point during the last month day, so the monthly bill will always include some leftovers from the previous month and will always miss some cost from the end of the billing month. Cloudyn always calculates full day usage since at the time of Cloudyn’s calculation full usage data is already available.
* Partner Center presents costs according to CSP’s time zone. Cloudyn always calculates daily costs in UTC time.
* CSP may be charged in local currency. Cloudyn will always calculate costs in USD and the pricing differences may be more than the exchange rate differences. Usually Cloudyn’s cost estimation is within 1-1.5% of the total monthly cost.

**Note**: If the EA number has changed, you will need to update the same in Cloudyn as well else you might not be able to see the data in Cloudyn reports.

Refer to the [FAQ: How to resolve apparent billing discrepancies between an Azure bill and Cloudyn reports](https://social.msdn.microsoft.com/Forums/azure/en-US/780bb6d5-99da-487f-96bb-849a83b45add/faq-how-to-resolve-apparent-billing-discrepancies-between-an-azure-bill-and-cloudyn-reports?forum=Cloudyn) to help troubleshoot your issue.

## **Recommended Documents**

* [Cloudyn Overview](https://docs.microsoft.com/azure/cost-management/overview)<br>
* [Cloudyn Pricing](https://azure.microsoft.com/pricing/details/cost-management)<br>
* [Cloudyn regional availability](https://azure.microsoft.com/global-infrastructure/services/)<br>
* [Cloudyn Training videos](https://docs.microsoft.com/azure/cost-management/ref-videos)<br>
