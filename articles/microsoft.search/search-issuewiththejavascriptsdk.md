<properties
	pageTitle="Development/Issue with the JavaScript or TypeScript SDK"
	description="Development/Issue with the JavaScript or TypeScript SDK"
	service="microsoft.search"
	resource="searchservices"
	authors="dereklegenzoff"
	ms.author="delegenz"
	selfHelpType="resource"
	supportTopicIds="32781149"
	displayOrder="2"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="search-issuewiththejavascriptsdk"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue with the JavaScript or TypeScript SDK

## **Recommended Steps**

* The Azure Cognitive Search JavaScript/TypeScript SDK has two libraries.  Make sure you're using the correct library for the operation that you'd like to perform:

	* [Client library: @azure/search-documents](https://docs.microsoft.com/javascript/api/overview/azure/search-documents-readme?view=azure-node-latest) to execute indexing and search operations on an Azure Cognitive Search index
	* [Management library: @azure/arm-search](https://docs.microsoft.com/javascript/api/overview/azure/search/management?view=azure-node-latest) to provision a new service, manage api-keys, and adjust resources

* Upgrade to the latest version of the Azure Cognitive Search JavaScript/TypeScript SDKs from [npm](https://www.npmjs.com/package/@azure/search-documents) for fixes and improvements
* If you encounter a bug, create an issue on [GitHub](https://github.com/Azure/azure-sdk-for-js/issues) and mention "Azure Cognitive Search" in the title
* To provide feedback for a future update of the SDK, see our [feedback page](https://feedback.azure.com/forums/263029-azure-search)

## **Recommended Documents**

* [JavaScript quickstart](https://docs.microsoft.com/azure/search/search-get-started-javascript)<br>
* [JavaScript/TypeScript samples](https://docs.microsoft.com/azure/search/samples-javascript)<br>
* [JavaScript/TypeScript SDK reference documentation](https://azure.github.io/azure-sdk-for-js/search.html)<br>
* [@azure/search-documents on npm](https://www.npmjs.com/package/@azure/search-documents)<br>
* [@azure/arm-search on npm](https://www.npmjs.com/package/@azure/arm-search)
