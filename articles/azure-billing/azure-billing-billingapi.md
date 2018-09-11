<properties
	pageTitle="Billing API"
	description="Billing API"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599494"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public"
/>

# Billing API

**Currently Azure offers the following APIs:**

* **Invoice**: This API allows you to Access your Azure invoice in PDF Format. The information returned by the invoice API is the exact same PDF invoice file that is available in the portal. There should be no difference regarding the use of this API compared to the information in the normal monthly invoice. Once the [opt-in has been complete](https://docs.microsoft.com/azure/billing/billing-manage-access#opt-in), download invoices using the preview version of [Invoice API](https://docs.microsoft.com/rest/api/billing)<br>
Learn more : [Azure Invoice Download (API)](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview#azure-invoice-download-api-preview).

* **RateCard**: The [Azure Resource RateCard API](https://msdn.microsoft.com/library/azure/mt219005) can be used to get the meter / resource metadata information along with prices used in a given subscription by Offer ID, Currency, Locale, Region.
Sources for parameters for Ratecard : There are presently no APIs which will get the parameters for an existing subscription. It needs to be obtained manually for input into the APIs.
  * OfferDurableId : [Microsoft Azure Offer Details](https://azure.microsoft.com/support/legal/offer-details/) lists all offers. "MS-AZR-" needs to be added to the beginning of the offer number from the table. (Example: MS-AZR-0003P)
  * Currency: [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) lists ISO currency codes. Not all countries may be represented in this API.
  * Locale
  * Region Info <br>
Learn more : [Azure Resource RateCard API](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview#azure-resource-ratecard-api-preview)

* **UsageAggregates**: The [UsageAggregates API](https://docs.microsoft.com/previous-versions/azure/reference/mt219003(v=azure.100)) allows you get consumption data for an Azure subscription. It returns all the usage data incurred on an Azure subscription and NOT JUST the usage data that was considered for billing – this might include any usage at the end of the billing cycle that was discarded due to lateness. It allows you to query aggregate Azure subscription consumption data by:
  * Start and end date/time
  * Aggregation granularity (ie: daily, hourly)
  * Instance level detail (ie: for multiple instances of the same resource)<br>
Learn more: [Azure Resource Usage API](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview#azure-resource-usage-api-preview)

**Partner Solutions**<br>
[Cloud Cruiser and Microsoft Azure Billing API Integration](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-partner-solution-cloudcruiser) describes how [Cloud Cruiser's Express for Azure Pack](http://www.cloudcruiser.com/partners/microsoft/) works directly from the Windows Azure Pack (WAP) portal. You can seamlessly manage both the operational and financial aspects of the Microsoft Azure private or hosted public cloud from a single user interface.

## **Recommended documents**

* [Azure Billing REST API](https://docs.microsoft.com/rest/api/billing/)
* [Partner solution - Cloud Cruiser](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-partner-solution-cloudcruiser)
* [Get consumption data for an Azure subscription](https://docs.microsoft.com/previous-versions/azure/reference/mt219001(v=azure.100)#frequently-asked-questions)
* [Billing- Invoices](https://docs.microsoft.com/rest/api/billing/invoices)
