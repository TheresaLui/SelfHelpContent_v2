<properties
	pageTitle="azure Cost Management API issues"
	description="azure budget api issues-Cost Management API issues"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615281"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="5a3c8fec-59d4-4d8b-a95f-8526cc35494d"
	ownershipId="ASMS_Billing"
/>

# Azure Cost Management API Issues

The Azure Cost Management APIs provide the ability to explore cost and usage data via multidimensional analysis, where creating customized filters and expressions allow you to answer consumption related questions for your Azure resources. These APIs are currently available for Azure Enterprise customers.

Please refer to the following information on the REST API options:

**REST Operation Groups**

  * [Dimensions](https://docs.microsoft.com/rest/api/cost-management/dimensions): Provides operations to get supported dimensions for your usage under a variety of scopes. Using the Dimensions API, you can retrieve a list of dimensions that can be used as inputs for generating queries with the Query API.<br>
  * [Query](https://docs.microsoft.com/rest/api/cost-management/query): Provides operations to get aggregated cost and usage data based on the query you supply. Using the Query API, you can specify your desired filtering, sorting and grouping on all available dimensions (which are accessed from the Dimensions API).<br>
  * [Budgets API v1](https://docs.microsoft.com/rest/api/consumption/budgets): Provides operations to create and update budgets. Using the Budgets API, you can set a budget threshold and configure multiple alerts to fire as you approach that threshold. Alerts can trigger an email or an Azure Action Group to perform automation.<br>
  * [Budgets API v2](https://github.com/Azure/azure-rest-api-specs/blob/master/specification/cost-management/resource-manager/Microsoft.CostManagement/preview/2019-04-01-preview/examples/CreateOrUpdateBudget.json): Create budgets with greater cost filtering capabilities than v1. Filtering aligns to the contract used in our Query and Dimensions APIs. This is the recommended budgets API to use moving forward. 

## **Recommended Documents**

* [Automation and offline analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis#automation-and-offline-analysis)<br>
* [Migrate from Enterprise Agreement to Microsoft Customer Agreement APIs](https://docs.microsoft.com/azure/cost-management/migrate-cost-management-api)<br>
* [What is Azure Cost Management?](https://docs.microsoft.com/azure/cost-management-billing/cost-management-billing-overview)<br>
* [Azure Cost Management REST API](https://docs.microsoft.com/rest/api/cost-management/)<br>
* [Azure Consumption REST API documentation](https://docs.microsoft.com/rest/api/consumption/)<br>
* [Azure Consumption REST API](https://docs.microsoft.com/rest/api/consumption/)<br>
* [Explore and analyze costs with Cost Analysis](https://docs.microsoft.com/azure/cost-management-billing/costs/quick-acm-cost-analysis)<br>
* [Azure Cost Management - Pricing](https://azure.microsoft.com/services/cost-management/)<br>
