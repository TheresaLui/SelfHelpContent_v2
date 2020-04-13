<properties
	pageTitle="Issue indexing a SQL data source"
	description="Issue indexing a SQL data source"
	service="microsoft.search"
	resource="searchservices"
	authors="luiscabrer"
	ms.author="luisca"
	selfHelpType="resource"
	displayOrder="7"
	supportTopicIds="32681365"
	resourceTags=""
	productPesIds="15568"
	articleId="sql-datasource"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue indexing a SQL data source

## **Recommended Steps**

If you are having trouble indexing a SQL data source, you may want to ensure that:

1. Your data is populated in the database
1. Your connection string is valid
1. The types in your database are supported by Azure Search. See the full list of supported types [here](https://docs.microsoft.com/azure/search/search-howto-connecting-azure-sql-database-to-azure-search-using-indexers#TypeMapping).
1. No firewall is preventing communication between Azure Search and the database
1. If you want to connect to SQL Server on a virtual machine, please follow [this guidance](https://docs.microsoft.com/azure/search/search-howto-connecting-azure-sql-iaas-to-azure-search-using-indexers)


If change detection is not working for you:

1. Make sure to enable [change tracking](https://docs.microsoft.com/sql/relational-databases/track-changes/enable-and-disable-change-tracking-sql-server?view=sql-server-2017) in your database
1. Confirm you meet the database version requirements:

	* SQL Server 2012 SP3 and later, if you're using SQL Server on Azure VMs
	* Azure SQL Database V12, if you're using Azure SQL Database

1. Ensure the primary key is not a composite primary key (a primary key containing more than one column) on the table
1. If your data source is a *view* (as opposed to a *table*), you won’t be able to use SQL Server integrated change detection to refresh an index with incremental changes

## **Recommended Documents**

* [Crawl a SQL database using Azure Search Indexers](https://docs.microsoft.com/azure/search/search-indexer-tutorial) <br>
* [Configure a connection from an Azure Search indexer to SQL Server on an Azure VM](https://docs.microsoft.com/azure/search/search-howto-connecting-azure-sql-iaas-to-azure-search-using-indexers) <br>
* [How to upload documents using indexers from the Azure Portal](https://azure.microsoft.com/documentation/articles/search-import-data-portal/) <br>
* [Capture changes using Azure SQL Integrated Change Tracking](https://docs.microsoft.com/azure/search/search-howto-connecting-azure-sql-database-to-azure-search-using-indexers#capture-new-changed-and-deleted-rows)
