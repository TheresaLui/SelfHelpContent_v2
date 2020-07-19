<properties
	pageTitle="Development/Issue with the .Net SDK"
	description="Development/Issue with the .Net SDK"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	ms.author="mcarter"
	selfHelpType="resource"
	supportTopicIds="32681376"
	displayOrder="2"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="search-issuewiththedotnetsdk"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue with the .Net SDK

## **Recommended Steps**

* The Azure Search .Net SDK has two libraries.  Please make sure you are using the correct library for the operation you'd like to perform:

	* [Client library](https://www.nuget.org/packages/Microsoft.Azure.Search) to execute indexing and search operations on an Azure Search index
	* [Management library](https://www.nuget.org/packages/Microsoft.Azure.Management.Search) to provision a new service, manage api-keys, and adjust resources

* Upgrade to the latest version of the Azure Search .NET SDKs from Nuget.org for fixes and improvements
* If you encounter a bug, please create an issue on [GitHub](https://github.com/azure/azure-sdk-for-net/issues) and mention "Azure Search" in the title
* If you would like to provide feedback for a future update of the SDK, see our [feedback page](https://feedback.azure.com/forums/263029-azure-search)

## **Recommended Documents**

* [How to use Azure Search from a .NET Application](https://docs.microsoft.com/azure/search/search-howto-dotnet-sdk)<br>
* [Quickstart: Create an Azure Search index in C# using the .NET SDK](https://docs.microsoft.com/azure/search/search-get-started-dotnet)<br>
* [Azure Search .NET SDK Reference](https://docs.microsoft.com/dotnet/api/microsoft.azure.search?view=azure-dotnet)<br>
* [Azure Search libraries for .NET](https://docs.microsoft.com/dotnet/api/overview/azure/search?view=azure-dotnet)<br>
* [Upgrade to the latest Azure Search .NET SDK release](https://docs.microsoft.com/azure/search/search-dotnet-sdk-migration-version-10)
* [Sample: Create and manage an Azure Search service](https://github.com/Azure-Samples/search-dotnet-management-api)
