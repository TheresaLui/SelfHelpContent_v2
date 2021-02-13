<properties
	pageTitle="Development/Issue with the Python SDK"
	description="Development/Issue with the Python SDK"
	service="microsoft.search"
	resource="searchservices"
	authors="dereklegenzoff"
	ms.author="delegenz"
	selfHelpType="resource"
	supportTopicIds="32781150"
	displayOrder="2"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="search-issuewiththepythonsdk"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue with the Python SDK

## **Recommended Steps**

* The Azure Cognitive Search Python SDK has two libraries.  Please make sure you are using the correct library for the operation you'd like to perform:

	* [Client library: azure-search-documents](https://docs.microsoft.com/python/api/overview/azure/search-documents-readme?view=azure-python) to execute indexing and search operations on an Azure Cognitive Search index
	* [Management library: azure-mgmt-search](https://docs.microsoft.com/python/api/overview/azure/search/management?view=azure-python) to provision a new service, manage api-keys, and adjust resources

* Upgrade to the latest version of the Azure Cognitive Search Python SDKs from pypi.org for fixes and improvements
* If you encounter a bug, please create an issue on [GitHub](https://github.com/azure/azure-sdk-for-python/issues) and mention "Azure Cognitive Search" in the title
* To provide feedback for a future update of the SDK, see our [feedback page](https://feedback.azure.com/forums/263029-azure-search)

## **Recommended Documents**

* [Python Quickstart](https://docs.microsoft.com/azure/search/search-get-started-python)<br>
* [Python samples](https://docs.microsoft.com/azure/search/samples-python)<br>
* [Python SDK reference documentation](https://azuresdkdocs.blob.core.windows.net/$web/python/azure-search-documents/latest/index.html)<br>
* [azure-search-documents on pypi](https://pypi.org/project/azure-search-documents/)<br>
* [azure-mgmt-search on pypi](https://pypi.org/project/azure-mgmt-search/)
