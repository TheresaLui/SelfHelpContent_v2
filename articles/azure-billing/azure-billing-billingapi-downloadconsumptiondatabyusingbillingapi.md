<properties
	pageTitle="Download consumption data by using Billing API"
	description="Download consumption data by using Billing API"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599495"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="986c8067-48e4-487b-ae3f-a6315cf6a0f5"
	ownershipId="ASMS_Billing"
/>

# Download consumption data by using Billing API

Azure Billing APIs can be used to pull usage and resource data into your preferred data analysis tools. The **Azure Resource Usage API** and **Azure Resource RateCard** API can help accurately predict and manage costs. The APIs are implemented as a Resource Provider and part of the family of APIs exposed by the Azure Resource Manager.

## **Recommended Steps**

* Use the [Azure Resource Usage API](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview#azure-resource-usage-api-preview) to get the list of available Azure resources and estimated pricing information for each
* Use [Azure Resource RateCard API](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview#azure-resource-ratecard-api-preview) to get your estimated Azure consumption data<br>

	**Note**: Support for Pay-as-you-go, MSDN, Monetary commitment, and Monetary credit offers (EA and [CSP](https://docs.microsoft.com/azure/cloud-solution-provider/billing/azure-csp-pricelist#get-prices-by-using-the-azure-rate-card) not supported)

* [Azure Invoice Download API](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview#azure-invoice-download-api-preview) allows you to Access your Azure invoice in PDF Format once the [opt-in has been complete](https://docs.microsoft.com/azure/billing/billing-manage-access#opt-in). It can be used to pull usage and resource data into preferred data analysis tools.

	**Note**: This feature is in first version of preview and may be subject to backward-incompatible changes. Currently, it's not available for certain subscription offers (EA, CSP, AIO not supported) and Azure Germany.

* The Azure Billing APIs can be used to programmatically get insights into Azure usage
* [Reporting APIs for EA customers - Usage Details](https://docs.microsoft.com/rest/api/billing/enterprise/billing-enterprise-api-usage-detail) offers a daily breakdown of consumed quantities and estimated charges by an Enrollment. The result also includes information on instances, meters, and departments. The API can be queried by Billing period or by a specified start and end date

## **Recommended Documents**

* [Azure Billing REST API](https://docs.microsoft.com/rest/api/billing/)
* [Azure Billing API overview](https://docs.microsoft.com/azure/billing/billing-usage-rate-card-overview)
* [Azure Resource Manager overview](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-overview)
* [REST API Browser](https://docs.microsoft.com/rest/api/?view=Azure)
