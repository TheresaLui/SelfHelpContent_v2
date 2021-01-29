<properties
	pageTitle="Issue indexing an Azure Blob data source"
	description="Issue indexing an Azure Blob data source"
	service="microsoft.search"
	resource="searchservices"
	authors="vkurpad"
	ms.author="vikurpad"
	selfHelpType="resource"
	displayOrder="15"	
	supportTopicIds="32681363"
	resourceTags=""
	productPesIds="15568"
	articleId="azure-blob-datasource"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue indexing an Azure Blob data source

## **Recommended Steps**

If you are having trouble indexing an Azure Blob data source, you may want to ensure that:

1. Your files are in a [supported format](https://docs.microsoft.com/azure/search/search-howto-indexing-azure-blob-storage)
1. The data source properties (name, type, credentials, container) are set correctly as described [here](https://docs.microsoft.com/azure/search/search-howto-indexing-azure-blob-storage)
1. The storage account is not encrypted or protected with a firewall

Depending on your security requirements, you may also want to consider using [managed identity](https://docs.microsoft.com/azure/search/search-howto-managed-identities-storage) to connect to your Azure Blob data source.

## **Recommended Documents**

* [Index Azure Blob storage with Azure Search](https://docs.microsoft.com/azure/search/search-howto-indexing-azure-blob-storage)
* [Set up a connection to an Azure Storage account using a managed identity](https://docs.microsoft.com/azure/search/search-howto-managed-identities-storage)
