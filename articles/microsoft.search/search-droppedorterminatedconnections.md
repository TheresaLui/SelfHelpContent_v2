<properties
	pageTitle="Connectivity/Dropped or terminated connections"
	description="Connectivity/Dropped or terminated connections"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	ms.author="mcarter"
	selfHelpType="generic"
	displayOrder="27"
	supportTopicIds="32681346"
	resourceTags=""
	productPesIds="15568"
	articleId="search-droppedorterminatedconnections"
	cloudEnvironments="public, Fairfax"
	ownershipId="AzureSearch_AzureSearch"
/>

# Dropped or terminated connections

An established connection to an Azure Cognitive Search service can be terminated for multiple reasons, including client connection timeouts, changes to the server configuration, network failures, service updates, and so on. Please work through the step below for a first level of troubleshooting for your connection issue.

## **Recommended Steps**

* Try to reconnect to your search service URL directly using the SearchIf you are not able to reconnect, please switch to the problem subtype *Database is currently unavailable* to troubleshoot intermittent connection problems.
* Ensure that your service endpoint is not private.  [Configure a private endpoints](https://aka.ms/acsprivatelink) for a secure connection to you Azure Cognitive Search service.
* If you have IP whitelisting enabled, [set up additional firewall rules](https://docs.microsoft.com/en-us/rest/api/searchmanagement/2019-10-01-preview/createorupdate-service#iprule) to allow your client's IP address
* All client-to-service Azure Cognitive Search interactions require [SSL/TLS 1.2 or higher](https://docs.microsoft.com/en-us/security/solving-tls1-problem). To ensure your client applications remain secure, we recommend the TLS version should not be hardcoded.  [Learn more](https://docs.microsoft.com/en-us/dotnet/framework/network-programming/tls)

## **Recommended Documents**

* [Security and data privacy in Azure Search](https://docs.microsoft.com/azure/search/search-security-overview#encrypted-transmission-and-storage)<br>
* [HTTP status codes (Azure Search)](https://docs.microsoft.com/rest/api/searchservice/http-status-codes)<br>
