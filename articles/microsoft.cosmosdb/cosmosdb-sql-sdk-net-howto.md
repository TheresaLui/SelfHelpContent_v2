<properties 
	pageTitle="SDK .NET- How to" 
	description="SDK .NET- How to" 
	service="microsoft.documentdb" 
	resource="databaseAccounts" 
	authors="jimsch" 
	ms.author="jimsch" 
	selfHelpType="generic" 
	supportTopicIds="32783720"
	resourceTags="" 
	productPesIds="15585" 
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sql-sdk-net-howto" 
	displayOrder="412" 
	category="SDK Issues" 
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB .NET SDK How-to   
Most users are able to resolve their SDK case using the steps below. The Recommended Documents section contain further information for more troubleshooting scenarios.

## **Recommended Steps**  

### **Use latest SDK versions and singleton client**  
Always ensure you are using the latest SDK:
* [Azure Cosmos DB .NET SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet-standard)
<br>Please ensure you are using singleton (one client instance for the lifetime of the application) client.

### **Known Issues and Solutions**  
Review the Github issues links below for your SDK platform to see if there is a known bug, and status of the fix from the Azure Cosmos DB team:
* [.NET SDK](https://github.com/Azure/azure-cosmos-dotnet-v3/issues)


### **Issues with Bulk Delete**
Performance issue while deleting documents in Cosmos DB.
* Restructuring the code to query the partition ids and fetch all the documents in that partition which meet your criteria. Then run the delete on all the matching documents within that partition. This will avoid the cross partition queries and the performance will improve. 
* Also please see [Usage of Bulk support](https://github.com/Azure/azure-cosmos-dotnet-v3/tree/master/Microsoft.Azure.Cosmos.Samples/Usage/BulkSupport)  

### **Is it advised to use both Pull (indexer) and Push (SDK) strategies on the same index?**
You can use both strategies but you should keep in mind that when indexer runs it will re-index the data based on the source so if push API is doing something differently than data source, indexer will overlap it or vice versa.
<br>If you are getting duplicated records, this may be due to the indexer will base64encode _rid, so if you base64encode and make sure that push API is getting same rid as indexer then you should not see duplicates. For additional information please see the following article [Create a target search index](https://docs.microsoft.com/azure/search/search-howto-index-cosmosdb#3---create-a-target-search-index)  



## **Recommended Documents**  

[Troubleshoot issues when using Azure Cosmos DB .NET SDK](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the .NET SDK with Azure Cosmos DB SQL API accounts.  

[FAQ](https://docs.microsoft.com/azure/cosmos-db/faq#sql-api-faq)
<br>Frequently asked questions about Cosmos DB SQL API.  

[How can I improve my database performance with .NET SDK?](https://docs.microsoft.com/azure/cosmos-db/performance-tips-dotnet-sdk-v3-sql)
<br>This article covers the most common improvements that will improve your application performance when using the .NET SDK.
