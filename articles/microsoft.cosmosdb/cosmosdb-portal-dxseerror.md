<properties
	pageTitle="Azure Cosmos DB error in data explorer"
	description="Error in Data Explorer"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="deborahc"
	ms.author="dech"
	selfHelpType="generic"
	supportTopicIds="32636780,32636790"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-portal-dxseerror"
/>

# I am getting an error when browsing data through Azure Cosmos DB Data Explorer

## **Recommenede Steps**

Before further troubleshooting, clear your browser cache and reload the page. This will ensure you are using the latest version of the Data Explorer.

Load the Data Explorer in Incognito or private browsing mode. If the issue does not occur there, then clearing your cache in your original browsing session and reloading will resolve the issue. If the issue continues to occur in Incognito mode, please contact us for support. 

### **Unable to view data in Data Explorer** 

If you are not able to view your data - databases, containers, and/or items (documents) from Data Explorer, check if Virtual Networks (VNET) is enabled for your Cosmos account. 

If VNET is enabled, navigate to the "Firewall and virtual networks" pane and ensure:

1. The setting "Allow access from Azure Portal" is enabled
1. If you are accessing the Portal from outside the VNET and want to view data, you will need to add your current IP Address to the Firewall. If you are within the VNET, only step 1 is required. 

If you have followed these steps and receive a 403 "Unable to proceed with the request. Please check the authorization claims to ensure the required permissions to process the request" error, please contact us for support and provide the ActivityId. 

If you do not have permission to view or change VNET/Firewall settings for your account, contact your Cosmos account owner to enable the above. 

### **Cannot view my MongoDB API data**

The Data Explorer uses the native SDK based on the Azure Cosmos DB Account API type to access the data from the service.

Using the Azure Cosmos DB SQL API SDK to perform CRUD operations against a MongoDB API account will not generate any errors. However, this would make the Data Explorer produce the internal server error when reading the data due to a mismatch in the data formats.

Use the native MongoDB SDKs to perform CRUD operations against your Azure Cosmos DB MongoDB API account. 

### **Query results not as expected**

By default, the Data Explorer returns query results in pages, with up to 100 results per page. To view additional pages of results, select the **"Load more"** button under the results tab. You can adjust the maximum number of results per page in the Data Explorer **Settings** tab. 

## **Recommended Documents**

* Review [Get started with Azure Cosmos DB MongoDB API](https://docs.microsoft.com/azure/cosmos-db/mongodb-introduction#how-to-get-started) for building MongoDB API applications


Review documentation on how [Virtual Network](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-vnet-service-endpoint) and [Firewall](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall) work with Azure Cosmos DB.
