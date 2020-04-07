<properties
	pageTitle="General Billing API and EA API questions"
	description="General Billing API and EA API questions"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599496"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="9b614f8f-088e-4048-bbac-24ce38f0c9cf"
	ownershipId="ASMS_Billing"
/>

# General Billing API and EA API questions

**General API FAQ:**

* **What permissions do I need to access Invoices?**<br>
The Azure Billing REST APIs are implemented as a Resource Provider as part of the Azure Resource Manager and share its dependencies. Access control for Azure Resource Manager uses the built-in Owner, Contributor, and Reader roles via the Role Based Access Control (RBAC) feature in the [Azure Preview portal](https://portal.azure.com/). You must make sure that the logged-in account is assigned one of those three roles for the specified subscription. By default, all service administrators and co-administrators are assigned the Owner role, and have implicit access. For details, see [Role-based access control](https://azure.microsoft.com/documentation/articles/role-based-access-control-configure/) in the [Microsoft Azure portal](https://azure.microsoft.com/documentation/articles/role-based-access-control-configure/).

* **Is it possible to derive or automatically supply the RateCard parameters (offer ID, currency, locale, region)?**<br>
We don't currently have a way to do this in RateCard, and as such all parameters are required.

* **Where can I get a list of offer Durable Ids?**<br>
[Offer details](https://azure.microsoft.com/support/legal/offer-details/) lists all offers. The offer number from the table must be prepended with "MS-AZR-" Eg: MS-AZR-0003P.

* **I'm calling ratecard through ARM (direct) with a CSP subscription and I'm getting an error?**<br>
CSP subscriptions must use partner ratecard to access ratecard.

* **The API can’t be consumed for Multi-Enrollment scenarios?**<br>
As of this time, that option is not available.

* **I need to associate Billing data and Monitoring data via the Billing API.**<br>
The option we have is via Azure Cost Management, because it’s a mix of Billing API and Monitoring API functions

* **Could we perform resource sizing via the API without using third-party software?**<br>
As of now this is not possible without using Azure Cost Management features.

* **Tags applied to Resource Groups are not showing in billing API report?**<br>
This is by design. Only tags applied to resources are visible in the report pulled via the Billing API.

* **My refresh is taking forever**<br>
Refresh in PowerBI will pull all the data from scratch and not just the data since the last import. This is time consuming and can take up to an hour if the volume of data is large

* **I’m unable to download EA MarketPlace cost via the Billing API**<br>
Both API v1 and v2 do not have one-time charges enabled. The product team is considering this feature but do not have a timeline available


## **Recommended Documents**

* [REST API Browser](https://docs.microsoft.com/rest/api/?view=Azure)
* [Azure Billing REST API](https://docs.microsoft.com/rest/api/billing/)
* [Azure Billing API Overview](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview#azure-resource-ratecard-api-preview)
* [Azure Invoice Download API](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview#azure-invoice-download-api-preview)
* [Azure Resource Usage API](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview#azure-resource-usage-api-preview)
* [Azure Resource RateCard API](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview#azure-resource-ratecard-api-preview)
