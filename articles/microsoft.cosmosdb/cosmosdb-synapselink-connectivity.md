<properties
	pageTitle="Azure Synapse Link for Cosmos DB - connectivity"
	description="Azure Synapse Link for Cosmos DB - connectivity"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32743028"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-connectivity"
	displayOrder="308"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Synapse Link for Azure Cosmos DB

Most users can resolve issues in Azure Synapse Link for Azure Cosmos DB by applying these answers to frequently asked questions.


## **Recommended Steps**  

### **Supported APIs**
Currently, Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview. For more information, contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.

### **Why would you use a managed virtual network in your workspace?**
Azure Cosmos DB users can enable private endpoints to protect network access for transactional store data. In Synapse Link, transactional store data is automatically replicated to the analytical store. Users want to restrict network access to data in the analytical store, too, by limiting it to Synapse managed networks. We are enabling network isolation for the Azure Cosmos DB analytical store by using managed private endpoints. You can enable these in Synapse managed virtual networks.  

### **Why can't I access the Cosmos DB analytical store by using a Synapse SQL dedicated pool?**
Only Synapse SQL serverless pool and Synapse Spark pool are currently supported. Synapse SQL dedicated pool is not supported.  

### **Why Can't I access the Cosmos DB analytical store by using Synapse Studio in another subscription**  
When you try to access Cosmos DB analytical store from a Synapse in other subscription, you receive the following error message: "An error occurred while calling... responseBody = {'code':'Forbidden','message':'Request originated from client IP ... through public internet. This is blocked by your Cosmos DB account firewall settings... ."
This error occurs because your IP address must be present in the firewall settings of the Cosmos account that you want to access. To fix this error, [follow these instructions](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall#allow-requests-from-global-azure-datacenters-or-other-sources-within-azure).

### **Which Azure Cosmos DB APIs are supported by private endpoints for Synapse Link?** 
Private endpoints are applicable to APIs that are supported by Synapse Link. Those are SQL API and MongoDB.

### **Is it possible to enable analytical private endpoints from a user's VNet?**
No. Users can enable only an analytical private endpoints from Synapse Studio on a Synapse-managed VNet.

### **If a user already has a private endpoint enabled on Cosmos DB from their own VNet, how does this affect the analytical store?**  
- This message means that network access for the analytical store data is not protected by that private endpoint.
- To use this account in Spark, and add network isolation, users should map this account as a managed private endpoint.
- To use this account in SQL Serverless, users should also enable the MSI bypass setting for the Synapse workspace on the Cosmos DB account.

### **If the managed VNet has data-exfiltration protection turned on, why can't I reach other public endpoints?**  
- For Synapse Spark, if the managed VNet has data-exfiltration protection turned on, access for read and write operations is allowed to only private endpoints that are enabled in that VNet.
- For Synapse SQL serverless, because this is a multi-tenant service that is not part of a VNet, reads are allowed to any destination, including public endpoints. However, data-exfiltration is guaranteed by allowing the writes (CETAS, for example) to private endpoints that are enabled in that VNet.  

### **I've enabled analytical private endpoint for Synapse Link. Why can't I query it from Synapse SQL serverless? Do I have to enable MSI allow lists for Synapse SQL serverless?**
SQL serverless is a multi-tenant service that is not part of the Synapse-managed VNet. To get access to the Cosmos DB account that is locked by private endpoints, users must allow Synapse Workspace resourceID as “networkaclbypass.” Users should still map the analytical endpoint to the Synapse-managed VNet to make sure the analytical store data is network-isolated.  

### **Can I enable multiple private endpoints for the same account, in the same Synapse VNet?**  
Yes. You can enable private endpoints for OLTP (SQL or MongoDB) and the analytical store. However, you can enable only one private endpoint of each type (OLTP or analytical) for a given account in a Synapse VNet.

### **How can I protect my data in power Bi by using Synapse?**  
Users build BI dashboards by using SQL views, and build on top of Cosmos DB analytical store by using T-SQL/SQL serverless. To enable network isolation on power BI:  
- Turn on “no public access” on BI, and connect to it over a private link from a VNet.
- Enable a private endpoint to SQL serverless in Synapse. Approve the endpoint request in a Synapse workspace.

By doing this, users can now privately access the SQL views that are built on the analytical store to render in BI.


### **Why is Spark data not refreshing?**
About the **loading to Spark DataFrame** message, the fetched metadata is cached throughout the lifetime of the Spark session. Therefore, later actions that are invoked on the DataFrame are evaluated against the snapshot of the analytical store at the time of DataFrame creation.
On the other hand, in the case of **creating a Spark table**, the metadata of the analytical store state is not cached in Spark but is reloaded on every Spark SQL query execution against the Spark table.
Therefore, you can choose between loading to Spark DataFrame and creating a Spark table based on whether you want your Spark analysis to be evaluated against a fixed snapshot of the analytical store or against the latest snapshot of the analytical store, respectively. [Learn more](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/how-to-query-analytical-store-spark).

### **"Why am I receiving a "File cannot be opened" error?**
If you receive a "Failed to execute query. File... cannot be opened because it does not exist or is used by another process" error message, check your permissions on the Azure Data Lake Store that supports your Synapse workspace. For more information, see [this quickstar topic](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-workspace#create-a-synapse-workspace).


## **Recommended documents**  

[Azure Synapse Link limits](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/concept-synapse-link-cosmos-db-support)
<br>his article describes the functionalities that are currently supported in Azure Synapse Link for Azure Cosmos DB.  

[Configure your Cosmos DB Firewall](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall#allow-requests-from-global-azure-datacenters-or-other-sources-within-azure)  
  
[Configure Cosmos DB Private Endpoints](https://docs.microsoft.com/azure/cosmos-db/analytical-store-private-endpoints)
<br>In this article, you will learn how to set up managed private endpoints for Azure Cosmos DB analytical store. 