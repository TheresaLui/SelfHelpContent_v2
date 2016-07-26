<properties
	pageTitle="My database is slow"
	description="My database is slow"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="AndrewHoh"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="databases"
	productPesIds=""
	cloudEnvironments="public"
/>

# My database is slow

## **Recommended steps**
To resolve common slowness issues, try one or more of the following steps.

* Install the most recent SDK. DocumentDB SDKs are constantly being improved to provide the best performance.
* Enable [direct connectivity](https://msdn.microsoft.com/library/azure/microsoft.azure.documents.client.connectionmode.aspx) when setting up your DocumentClient.
* Increase the number of threads/tasks to decrease the wait time while fulfilling requests.
* For .NET, increase the [System.Net MaxConnections](https://msdn.microsoft.com/library/azure/microsoft.azure.documents.client.connectionpolicy.maxconnectionlimit.aspx#P:Microsoft.Azure.Documents.Client.ConnectionPolicy.MaxConnectionLimit) to have multiple simultaneous connections to DocumentDB, which has a default of 50 threads for .NET SDK 1.8.0 and above.
* When possible, deploy your application and DocumentDB database to the same Azure region. For a ballpark comparison, calls to DocumentDB within the same region complete within 1-2ms, but latency between the West and East coast of the US is > 50ms.
* Trying increasing the allocated Request Units (RUs) for your collection. You can use the Portal to change the throughput by following these [instructions](https://azure.microsoft.com/documentation/articles/documentdb-performance-levels/#changing-performance-levels-using-the-azure-portal).

## **Recommended documents**
[Performance and scale testing with Azure DocumentDB](https://azure.microsoft.com/documentation/articles/documentdb-performance-testing/)
