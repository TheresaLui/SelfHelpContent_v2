<properties
	pageTitle="My queries are slow"
	description="My queries are slow"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="anhoh"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="databases"
	productPesIds=""
	cloudEnvironments="public"
/>

# My queries are slow

## **Recommended steps**
To resolve common slowness issues, try one or more of the following steps.

* Whenever possible, avoid full scans on the collection. All user defined functions (UDFs) and [built-in functions](https://azure.microsoft.com/en-us/documentation/articles/documentdb-sql-query/#built-in-functions) will scan across all documents within its scope. To optimize performance, add a WHERE clause to your queries with UDFs and built-in functions to reduce the scope of the query.
* Enable [direct connectivity](https://msdn.microsoft.com/library/azure/microsoft.azure.documents.client.connectionmode.aspx) when setting up your DocumentClient.
* Tune the page size for queries/read feeds for better performance using x-ms-max-item-count header. Read more under SDK Usage Tip #3 in [Performance Tips for Azure DocumentDB part 1](https://azure.microsoft.com/en-us/blog/performance-tips-for-azure-documentdb-part-1-2/).
* For partitioned collections, query in parallel to increase performance and leverage more throughput. [Example code](https://github.com/Azure/azure-documentdb-dotnet/blob/master/samples/code-samples/Queries/Program.cs#L664-L734) for .NET SDK 1.9.2 and above.

## **Recommended documents**
[Performance Tips for Azure DocumentDB - Part 1](https://azure.microsoft.com/en-us/blog/performance-tips-for-azure-documentdb-part-1-2/)
[SQL query and SQL syntax in DocumentDB](https://azure.microsoft.com/en-us/documentation/articles/documentdb-sql-query/)
