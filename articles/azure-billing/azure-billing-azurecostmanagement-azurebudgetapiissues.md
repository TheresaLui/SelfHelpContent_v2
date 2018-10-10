<properties
	pageTitle="azure budget api issues"
	description="azure budget api issues"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615281"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public"
/>

# Azure Budget API Issues

The Azure Cost Management APIs provide the ability to explore cost and usage data via multidimensional analysis, where creating customized filters and expressions allow you to answer consumption related questions for your Azure resources. These APIs are currently available for Azure Enterprise customers.

**REST Operation Groups**

  * [Dimensions](https://docs.microsoft.com/rest/api/cost-management/dimensions): Provides operations to get supported dimensions for your usage under a variety of scopes. Using the Dimensions API, you can retrieve a list of dimensions that can be used as inputs for generating queries with the Query API.<br>
  * [Query](https://docs.microsoft.com/rest/api/cost-management/query): Provides operations to get aggregated cost and usage data based on the query you supply. Using the Query API, you can specify your desired filtering, sorting and grouping on all available dimensions (which are accessed from the Dimensions API).<br>  

## **Recommended documents**

* [Azure Cost Management REST API](https://docs.microsoft.com/rest/api/cost-management/)<br>
* [Azure Consumption REST API documentation](https://docs.microsoft.com/rest/api/consumption/)<br>
* [Azure Consumption REST API](https://docs.microsoft.com/rest/api/consumption/)<br>
* [What is Azure Cost Management ?](https://docs.microsoft.com/azure/cost-management/overview-cost-mgt)<br>
* [Explore and analyze costs with Cost Analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Azure Cost Management - Pricing](https://azure.microsoft.com/pricing/details/cost-management/)<br>
