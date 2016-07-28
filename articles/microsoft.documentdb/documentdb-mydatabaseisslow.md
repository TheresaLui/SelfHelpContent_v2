<properties
	pageTitle="My database is slow"
	description="My database is slow"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="AndrewHoh"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# My database is slow

## **Recommended steps**
To speed up your database, try one or more of the following steps.

* Install the latest DocumentDB SDK. DocumentDB SDKs are constantly being improved to provide the best performance. [Learn more](https://azure.microsoft.com/documentation/articles/documentdb-sdk-dotnet/)
* Use direct mode as your connection mode when configuring your connection policy. [Learn more](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#direct-connection)
* Increase the number of threads/tasks to decrease the wait time while fulfilling requests. [Learn more](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#increase-threads)
* For .NET, increase the *System.Net MaxConnections* to have multiple simultaneous connections to DocumentDB, which has a default of 50 threads for .NET SDK 1.8.0 and above. [Learn more](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#max-connection)
* When possible, deploy your application and DocumentDB database to the same Azure region. For a ballpark comparison, calls to DocumentDB within the same region complete within 1-2ms, but latency between the West and East coast of the US is more than 50ms. [Learn more](https://azure.microsoft.com/documentation/articles/documentdb-performance-tips/#same-region)
* Try increasing the allocated Request Units (RUs) for your collection. [Learn more](https://azure.microsoft.com/documentation/articles/documentdb-performance-levels/#change-throughput)

## **Recommended documents**
[Performance and scale testing with Azure DocumentDB](https://azure.microsoft.com/documentation/articles/documentdb-performance-testing/)
