<properties
	pageTitle="Authentication"
	description="Troubleshoot Azure Cosmos DB Authentication related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636770"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-authentication"
	displayOrder="60"
	category="Core (SQL)"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Authentication in Azure Cosmos DB
Most users are able to resolve their Authentication case using the steps below.

## **Recommended Steps**

### **TLS 1.2 on Azure Cosmos DB**

Cosmos DB supports TLS 1.2 and enforcement is based on the below factors
- The account should be enabled to only allow TLS 1.2 connection
- The Client SDK Version  

The enforcement plan is as follows
- All **new accounts created on or after 29th July 2020** would be **enforcing the connection** to be TLS 1.2
- All legacy database account  to which a client is using TLS 1.2 would be migrated to enforce the TLS 1.2 seamlessly.  This means any connection using TLS version lower than 1.2 will be rejected after the migration and the client would get a clear error message.
- Any legacy database account to which the client are not using TLS 1.2 would continue to work fine and no enforcement would be applied

<br>

### **How can you migrate your legacy account to enforce TLS 1.2?**   
Please file a support ticket with the Cosmos DB.



## **Recommended Documents**

[TLS 1.2 enforcement on Azure Cosmos DB](https://devblogs.microsoft.com/cosmosdb/tls-1-2-enforcement/)
<br>Microsoft Azure recommends all customers complete migration towards solutions that support transport layer security (TLS) 1.2 and make sure that TLS 1.2 is used by default.  

[Securing access to Azure Cosmos DB data](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data)
<br>This article provides an overview of securing access to data stored in Microsoft Azure Cosmos DB.  

[Access Control on Azure Cosmos DB Resources](https://docs.microsoft.com/rest/api/cosmos-db/access-control-on-cosmosdb-resources)
<br>Azure Cosmos DB is a globally distributed multi-model database with support for multiple APIs. This article covers the SQL API for Azure Cosmos DB.   

[Azure Cosmos DB database security](https://docs.microsoft.com/azure/cosmos-db/database-security)
<br>This article discusses database security best practices and key features offered by Azure Cosmos DB to help you prevent, detect, and respond to database breaches.