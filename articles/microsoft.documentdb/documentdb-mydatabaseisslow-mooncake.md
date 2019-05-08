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
	productPesIds="15585"
	cloudEnvironments="MoonCake"
	articleId="61352f97-502d-4ca1-b0d2-a0af6aa0294a"
/>

# My database is slow

## **Recommended steps**
To speed up your database, try one or more of the following steps.

* Install the latest DocumentDB SDK. DocumentDB SDKs are constantly being improved to provide the best performance.<br>
[DocumentDB SDK](https://docs.azure.cn/cosmos-db/documentdb-sdk-dotnet)
* Use direct mode as your connection mode when configuring your connection policy.<br>[Performance tips for DocumentDB - Direct Connectivity](https://docs.azure.cn/cosmos-db/performance-tips#direct-connection)
* Increase the number of threads/tasks to decrease the wait time while fulfilling requests.<br>[Performance tips for DocumentDB - Increase Threads](https://docs.azure.cn/cosmos-db/performance-tips#increase-threads)
* For .NET, increase the *System.Net MaxConnections* to have multiple simultaneous connections to DocumentDB, which has a default of 50 threads for .NET SDK 1.8.0 and above.<br>[Performance tips for DocumentDB - Max Connections](https://docs.azure.cn/cosmos-db/performance-tips#max-connection)
* When possible, deploy your application and DocumentDB database to the same Azure region. For a ballpark comparison, calls to DocumentDB within the same region complete within 1-2ms, but latency between the West and East coast of the US is more than 50ms.<br>[Performance tips for DocumentDB - Same Region](https://docs.azure.cn/cosmos-db/performance-tips#same-region)
* Try increasing the allocated Request Units (RUs) for your collection.<br>[Performance levels in DocumentDB - Changing the throughput of a collection](https://docs.azure.cn/cosmos-db/performance-levels#change-throughput)

## **Recommended documents**
[Performance and scale testing with Azure DocumentDB](https://docs.azure.cn/cosmos-db/performance-testing)
