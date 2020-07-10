<properties
	pageTitle="Setup and Configuration/Issue using the ARM template"
	description="Issue using the ARM template"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	ms.author="mcarter"
	selfHelpType="resource"
	displayOrder="56"
	supportTopicIds="32681372"
	resourceTags=""
	productPesIds="15568"
	articleId="search-issueusingthearmtemplate"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue using the ARM template

## **Recommended Steps**

There are two types of errors that are related to ARM template deployment:

* **Validation errors** from scenarios that can be determined before deployment. These include syntax errors in your template, or trying to deploy resources that would exceed your subscription quotas or limits defined by Azure Cognitive Search.
* **Deployment errors** arise from conditions that occur during the deployment process. They include trying to access a resource that is being deployed in parallel.

Refer to [Azure Resource Manager (ARM) documentation](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-troubleshoot) for more information about diagnosing common template deployment errors.

## **Recommended Documents**

* [Quickstart: Deploy Cognitive Search using a Resource Manager template](https://docs.microsoft.com/azure/search/search-get-started-arm)
* [Service limits in Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-limits-quotas-capacity)