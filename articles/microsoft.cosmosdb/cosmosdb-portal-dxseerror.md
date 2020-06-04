<properties
	pageTitle="Azure Cosmos DB error in data explorer"
	description="Error in Data Explorer"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="deborahc"
	ms.author="dech"
	selfHelpType="generic"
	supportTopicIds="32688846"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-portal-dxseerror"
	displayOrder="80"
	category="Portal"
	ownershipId="AzureData_AzureCosmosDB"
/>

# I am getting an error using Azure Cosmos DB Data Explorer, Metrics, or Notebooks

## **Recommended Steps**

* Before further troubleshooting, clear your browser cache and reload the page. This will ensure you are using the latest version of the Data Explorer.
* Load the Data Explorer in Incognito or private browsing mode. If the issue does not occur there, then clearing your cache in your original browsing session and reloading will resolve the issue. If the issue continues to occur in Incognito mode, please contact us for support. 


**Cosmos DB Data Explorer not loading and timeout error is thrown after a few minutes**
<br>Please try connecting to explorer using the [Sunset link](https://cosmos.azure.com/sunset/).  


### **Cannot view my MongoDB API data**
* The Data Explorer uses the native SDK based on the Azure Cosmos DB Account API type to access the data from the service
* Using the Azure Cosmos DB SQL API SDK to perform CRUD operations against a MongoDB API account will not generate any errors. However, this would make the Data Explorer produce the internal server error when reading the data due to a mismatch in the data formats.
* Use the native MongoDB SDKs to perform CRUD operations against your Azure Cosmos DB MongoDB API account  


### **Query results not as expected**  
By default, the Data Explorer returns query results in pages, with up to 100 results per page. To view additional pages of results, select the **"Load more"** button under the results tab. You can adjust the maximum number of results per page in the Data Explorer **Settings** tab.  


### **Enable Free Tier when creating a new account in the Azure Portal is not appearing. Where is the option?**
**Solution: ** You can have up to one Free Tier account in an Azure subscription. If the option does not appear, this means another account in the subscription is already enabled with Free Tier.

### Data Explorer does not load or show data  
**Solution:** Possibly there is a browser cache issue. Try cleaning your browser cache or try opening Data Explorer from an incognito tab.


### **Unable to view data, stored procedures, UDFs, or triggers in Data Explorer**
If you are not able to view your data including databases, containers, items (documents), stored procedures, UDFs, or triggers from Data Explorer, check if Virtual Networks (VNET) is enabled for your Cosmos account
* If VNET is enabled, navigate to the "Firewall and virtual networks" pane and ensure:
<br>The setting *Allow access from Azure Portal* is enabled
	
![throughput visual](https://docs.microsoft.com/azure/cosmos-db/media/how-to-configure-firewall/enable-azure-portal.png)  

If you are accessing the Portal from outside the VNET and want to view data, you will need to add your current IP Address to the Firewall. If you are within the VNET, only setting *Allow access from Azure Portal* is required.  
If you have followed these steps and receive a 403 "Unable to proceed with the request. Please check the authorization claims to ensure the required permissions to process the request" error, please contact us for support and provide the ActivityId of the message. The ActivityId can be found in the yellow notification bar at the bottom of the Data Explorer screen. 

**Note** If you do not have permission to view or change VNET/Firewall settings for your account, contact your Cosmos account owner to enable the above.  

## **Recommended Documents**  

[Enable built-in notebooks](https://docs.microsoft.com/azure/cosmos-db/enable-notebooks)
<br>This article describes how to enable this feature for your Azure Cosmos DB account.  

[How to use notebook features](https://docs.microsoft.com/azure/cosmos-db/use-notebook-features-and-commands)
<br>This article describes how to use built-in notebook commands and features to do common operations.  

[Virtual Networks](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-vnet-service-endpoint)
<br>You can configure Azure Cosmos DB accounts to allow access from only a specific subnet of an Azure virtual network.   

[How to configure IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall)
<br>Learn how you can set an IP firewall on the Azure Cosmos DB account using the following: 
* From the Azure portal 
* Declaratively by using an Azure Resource Manager template 
* Programmatically through the Azure CLI or Azure PowerShell by updating the ipRangeFilter property  

[Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs)
<br>Azure Cosmos DB provides language-integrated, transactional execution of JavaScript. When using the SQL API in Azure Cosmos DB, you can write stored procedures, triggers, and user-defined functions (UDFs) in the JavaScript language. You can write your logic in JavaScript that executed inside the database engine. You can create and execute triggers, stored procedures, and UDFs by using Azure portal, the JavaScript language integrated query API in Azure Cosmos DB or the Cosmos DB SQL API client SDKs.


