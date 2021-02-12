<properties
	pageTitle="Private Link in Azure Cosmos DB"
	description="Private Link in Azure Cosmos DB"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32738665,32738664"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-security-privatelink"
	displayOrder="162"
	category="Security"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Private Endpoints in Azure Cosmos DB

If you are using Private Endpoints to expose your Azure Cosmos DB account to a virtual network, most users are able to resolve their Cosmos DB related Private Endpoints issue using the steps below.


## **Recommended Steps**  

### Make sure the API and connection mode you are using are supported by Azure Cosmos DB private endpoints

### **API type**   

* **SQL (Core) API Gateway mode:** *Supported*  
* **SQL (Core) API Direct mode over TCP:** *In preview*  
* **SQL (Core) API Direct mode over HTTP:** *Unsupported*  
* **MongoDB API version 3.2:**  *Unsupported* - You can either create a new account using the version 3.6 of the Mongo API, or create a support ticket under Cosmos MongoDB to request your account to be migrated from version 3.2 to 3.6.  
* **MongoDB API version 3.6:**  *Supported*  
* **Cassandra API:** *Supported* 
* **Gremlin (graph) API:** *Supported* - If you are connecting to your Gremlin account through its SQL API endpoint, refer to SQL (Core) API above.  
* **Table API Gateway mode:** *Supported* - If you are connecting to your Table account through its SQL API endpoint, refer to SQL (Core) API above.  
* **Table API Direct mode over TCP:**  *In preview*


### **Check the connection status of your private endpoint**
From the Azure Portal, navigate to your private endpoint resource and verify its connection status. If it shows up as *Pending*, ask the owner of the Azure Cosmos DB account involved to approve it by going to *Private Endpoint Connections* section on the Azure Portal.  

### **Update your DNS when adding or removing regions**
If you are using Azure Private Zones as the local DNS in your virtual network, DNS entries do not get automatically updated when you add or remove regions to your Azure Cosmos DB account. [Please Follow these instructions](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-private-endpoints#update-a-private-endpoint-when-you-add-or-remove-a-region)  


## **Recommended Documents**
[How to Configure Azure Private Endpoint for an Azure Cosmos account](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-private-endpoints)
<br>This article describes the steps to create a private endpoint.   

[Connect privately to an Azure Cosmos account using Azure Private Link](https://docs.microsoft.com/azure/private-link/create-private-endpoint-cosmosdb-portal)
<br>In this article, you will learn how to create a VM on an Azure virtual network and an Azure Cosmos account with a Private Endpoint using the Azure portal. Then, you can securely access the Azure Cosmos account from the VM.  

