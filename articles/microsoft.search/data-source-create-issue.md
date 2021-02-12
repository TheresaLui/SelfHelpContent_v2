<properties
	pageTitle="Issue creating a data source"
	description="Issue creating a data source"
	service="microsoft.search"
	resource="searchservices"
	authors="MarkHeff"
	ms.author="maheff"
	selfHelpType="resource"
	supportTopicIds="32681354"
	displayOrder="33"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="data-source-create-issue"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue creating a data source

## **Recommended Steps**

If you are having trouble creating a data source, consider the following:

1. If you've received an error in the Azure Portal related to the data source connection make sure that the connection string is correct.
1. When creating a data source in the Azure Portal, make sure that your data source already has some data in it.
1. When using the REST API or .NET SDK, make sure that the data source type you've provided is one of the supported data source types.

## **Recommended Documents**

* [Create Data Source (REST API)](https://docs.microsoft.com/rest/api/searchservice/create-data-source)
* [DataSource Class (.NET SDK)](https://docs.microsoft.com/dotnet/api/microsoft.azure.search.models.datasource?view=azure-dotnet)