<properties
	pageTitle="My queries are slow"
	description="My queries are slow"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="AndrewHoh"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# My queries are slow

## **Recommended steps**
To speed up queries, try one or more of the following steps.

* Whenever possible, avoid full scans on the collection. All user defined functions (UDFs) and built-in functions will scan across all documents within the query scope; for example, *SELECT * FROM c* will have a broader query scope than *SELECT * FROM c.foo = 'bar'*. To optimize performance, add a WHERE clause to your queries with UDFs and built-in functions to reduce the query scope.<br>[SQL query and SQL syntax in DocumentDB - Built-in functions](https://azure.microsoft.com/documentation/articles/documentdb-sql-query/#built-in-functions)<br>[SQL query and SQL syntax in DocumentDB - Where clause](https://azure.microsoft.com/documentation/articles/documentdb-sql-query/#where-clause)
* Use direct mode as your connection mode when configuring your connection policy.<br>[Performance tips for DocumentDB - Direct Connectivity](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#direct-connection)
* Tune the page size for queries and read feeds for better performance using the x-ms-max-item-count header.<br>[Performance tips for DocumentDB - Tune Page Size](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#tune-page-size)
* For partitioned collections, query in parallel to increase performance and leverage more throughput.<br>[
GitHub DocumentDB .NET Sample Code for .NET SDK 1.9.2 and above](https://github.com/Azure/azure-documentdb-dotnet/blob/master/samples/code-samples/Queries/Program.cs#L664-L734)

## **Recommended documents**
[Performance Tips for DocumentDB](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/)<br>
[SQL query and SQL syntax in DocumentDB](https://azure.microsoft.com/documentation/articles/documentdb-sql-query/)
