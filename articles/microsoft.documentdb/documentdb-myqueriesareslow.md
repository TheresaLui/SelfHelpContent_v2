<properties
	pageTitle="My queries are slow"
	description="My queries are slow"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="AndrewHoh"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="databases"
	productPesIds=""
	cloudEnvironments="public"
/>

# My queries are slow

## **Recommended steps**
To speed up queries, try one or more of the following steps.

* Whenever possible, avoid full scans on the collection. All user defined functions (UDFs) and [built-in functions](https://azure.microsoft.com/en-us/documentation/articles/documentdb-sql-query/#built-in-functions) will scan across all documents within the query scope; for example, *SELECT * FROM c* will have a broader query scope than *SELECT * FROM c.foo = 'bar'*. To optimize performance, add a WHERE clause to your queries with UDFs and built-in functions to reduce the query scope. [Learn more](https://azure.microsoft.com/en-us/documentation/articles/documentdb-sql-query/#where-clause)
* Use direct mode as your connection mode when configuring your connection policy. [Learn more](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#direct-connection)
* Tune the page size for queries and read feeds for better performance using x-ms-max-item-count header. [Learn more](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#tune-page-size)
* For partitioned collections, query in parallel to increase performance and leverage more throughput. [Example code](https://github.com/Azure/azure-documentdb-dotnet/blob/master/samples/code-samples/Queries/Program.cs#L664-L734) for .NET SDK 1.9.2 and above.

## **Recommended documents**
[Performance Tips](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/)
[SQL query and SQL syntax in DocumentDB](https://azure.microsoft.com/en-us/documentation/articles/documentdb-sql-query/)
