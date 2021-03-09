<properties 
	pageTitle="SDK Python - Performance" 
	description="SDK Python- Performance" 
	service="microsoft.documentdb" 
	resource="databaseAccounts" 
	authors="jimsch" 
	ms.author="jimsch" 
	selfHelpType="generic" 
	supportTopicIds="32783726"
	resourceTags="" 
	productPesIds="15585" 
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sql-sdk-python-performance"
	displayOrder="433"
	category="SDK Issues"
	ownershipId="AzureData_AzureCosmosDB"
/>

#  Azure Cosmos DB SQL API high latency issues  
Most users are able to resolve their Python SDK Performance issue with the following steps.

## **Recommended Steps**  

### **Use latest SDK versions**
Always ensure you are using the latest SDK:
- [Azure Cosmos DB Python SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-python)
<br>Please ensure you are using singleton (one client instance for the lifetime of the application) client.

### **Known Issues and Solutions**
Review the Github issues links below for your SDK platform to see if there is a known bug, and status of the fix from the Azure Cosmos DB team:  
- [Python SDK Issues](https://github.com/Azure/azure-sdk-for-python/issues)
- [Python SDK Limitations](https://github.com/Azure/azure-sdk-for-python/tree/master/sdk/cosmos/azure-cosmos#limitations)


## **Recommended Documents**  

[FAQ](https://docs.microsoft.com/azure/cosmos-db/faq#sql-api-faq)
<br>Frequently asked questions about Cosmos DB SQL API.    

[Azure Cosmos DB Python SDK for SQL API: Release notes and resources](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-python)