<properties
	pageTitle="Development/Issue with the Java SDK"
	description="Development/Issue with the Java SDK"
	service="microsoft.search"
	resource="searchservices"
	authors="dereklegenzoff"
	ms.author="delegenz"
	selfHelpType="resource"
	supportTopicIds="32781148"
	displayOrder="2"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="search-issuewiththejavasdk"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue with the Java SDK

## **Recommended Steps**

* The Azure Cognitive Search Java SDK has two libraries.  Make sure you're using the correct library for the operation you'd like to perform:

	* [Client library: azure-search-documents](https://docs.microsoft.com/java/api/overview/azure/search-documents-readme?view=azure-java-stable) to execute indexing and search operations on an Azure Cognitive Search index
	* [Management library: azure-mgmt-search](https://docs.microsoft.com/java/api/overview/azure/search/resourcemanagement?view=azure-java-stable) to provision a new service, manage api-keys, and adjust resources

* Upgrade to the latest version of the Azure Cognitive Search Java SDKs from Maven for fixes and improvements
* If you encounter a bug, please create an issue on [GitHub](https://github.com/azure/azure-sdk-for-java/issues) and mention "Azure Cognitive Search" in the title
* To provide feedback for a future update of the SDK, see our [feedback page](https://feedback.azure.com/forums/263029-azure-search)

## **Recommended Documents**

* [Java Quickstart](https://docs.microsoft.com/azure/search/search-get-started-java)<br>
* [Java samples](https://docs.microsoft.com/azure/search/samples-java)<br>
* [Java SDK reference documentation](https://azure.github.io/azure-sdk-for-java/search.html)<br>
* [azure-search-documents on Maven](https://search.maven.org/artifact/com.azure/azure-search-documents)<br>
* [azure-mgmt-search on Maven](https://search.maven.org/artifact/com.microsoft.azure/azure-mgmt-search)
