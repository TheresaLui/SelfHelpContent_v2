<properties
	articleId="costanalysis-restoperationgroups"
	articleTags="costanalysis,rest"
	pageTitle="What REST Operation Groups are available?"
	description="REST operation groups"
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

# What REST Operation Groups are available?

* [Dimensions](https://docs.microsoft.com/rest/api/cost-management/dimensions): Provides operations to get supported dimensions for your usage under a variety of scopes. Using the Dimensions API, you can retrieve a list of dimensions that can be used as inputs for generating queries with the Query API
* [Query](https://docs.microsoft.com/rest/api/cost-management/query): Provides operations to get aggregated cost and usage data based on the query you supply. Using the Query API, you can specify your desired filtering, sorting and grouping on all available dimensions (which are accessed from the Dimensions API)
* [Budgets API v1](https://docs.microsoft.com/rest/api/consumption/budgets): Provides operations to create and update budgets. Using the Budgets API, you can set a budget threshold and configure multiple alerts to fire as you approach that threshold. Alerts can trigger an email or an Azure Action Group to perform automation

Budgets API v2: Create budgets with greater cost filtering capabilities than v1. Filtering aligns to the contract used in our Query and Dimensions APIs. This is the recommended budgets API to use moving forward

## **Recommended Documents**

* [Automation and offline analysis](https://docs.microsoft.com/azure/cost-management-billing/costs/quick-acm-cost-analysis#automation-and-offline-analysis)<br>
* [Migrate from Enterprise Agreement to Microsoft Customer Agreement APIs](https://docs.microsoft.com/azure/cost-management-billing/costs/migrate-cost-management-api)<br>
* [What is Azure Cost Management?](https://docs.microsoft.com/azure/cost-management-billing/cost-management-billing-overview)
