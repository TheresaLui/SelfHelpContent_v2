<properties
	pageTitle="My database is slow"
	description="My database is slow"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="anhoh"
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
* For .NET, increase the [System.Net MaxConnections](https://msdn.microsoft.com/en-us/library/system.net.configuration.connectionmanagementelement.maxconnection(v=vs.110).aspx) per host to have multiple simultaneous connections to DocumentDB, which has a default of 50 threads for .NET SDK 1.8.0 and above.
* When possible, deploy your application and DocumentDB database to the same Azure region. For a ballpark comparison, calls to DocumentDB within the same region complete within 1-2ms, but latency between the West and East coast of the US is > 50ms.

## **Recommended documents**
[Performance and scale testing with Azure DocumentDB](https://azure.microsoft.com/documentation/articles/documentdb-performance-testing/)
