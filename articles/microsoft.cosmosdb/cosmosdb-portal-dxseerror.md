<properties
	pageTitle="Azure Cosmos DB error in data explorer"
	description="Error in Data Explorer"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="deborahc"
	ms.author="dech"
	selfHelpType="resource"
	supportTopicIds="32681013"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-portal-dxseerror"
	displayOrder="80"
	category="Portal"
/>

# I am getting an error using Azure Cosmos DB Data Explorer, Metrics, or Notebooks

## **Recommended Steps**

* Before further troubleshooting, clear your browser cache and reload the page. This will ensure you are using the latest version of the Data Explorer.
* Load the Data Explorer in Incognito or private browsing mode. If the issue does not occur there, then clearing your cache in your original browsing session and reloading will resolve the issue. If the issue continues to occur in Incognito mode, please contact us for support. 

**Unable to view data, stored procedures, UDFs, or triggers in Data Explorer** 

* If you are not able to view your data including databases, containers, items (documents), stored procedures, UDFs, or triggers from Data Explorer, check if Virtual Networks (VNET) is enabled for your Cosmos account
* If VNET is enabled, navigate to the "Firewall and virtual networks" pane and ensure:

	1. The setting "Allow access from Azure Portal" is enabled
	1. If you are accessing the Portal from outside the VNET and want to view data, you will need to add your current IP Address to the Firewall. If you are within the VNET, only step 1 is required. 

	If you have followed these steps and receive a 403 "Unable to proceed with the request. Please check the authorization claims to ensure the required permissions to process the request" error, please contact us for support and provide the ActivityId of the message. The ActivityId can be found in the yellow notification bar at the bottom of the Data Explorer screen. 

* If you do not have permission to view or change VNET/Firewall settings for your account, contact your Cosmos account owner to enable the above

### **Metrics**

**Metrics show throttling (429) but chart shows consumed throughput doesn't exceed provisioned throughput** 

- Scenario: You are seeing throttling (429) in Metrics, but the **Max consumed RU/s per partition key range** chart shows you are not exceeding the provisioned throughput on your database or container:

    -  By default, the Azure Cosmos DB client SDKs for SQL API handle 429s by retrying up to 9 times or 30 seconds. These 429s may never be surfaced to your application, but will still be reflected in the portal metrics.
    - Stored procedures with heavy read or query operation may result in 429s, but may not show as exceeding the provisioned RU in the database or container.
    - As a [best practice](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs), stored procedures should be used for write operations that require ACID transactions against a single partition key value. Perform read and query operations using the client SDKs for best performance and RU utilization.

**Metrics show throttling (429) at account level, but no throttles for individual databases or containers** 

- Scenario: You are seeing throttles (429) when viewing the metrics at the account level (when Database(s) and Container(s) are filtered to ALL), but not seeing 429s when filtered to any individual database or container:

    - When performing a high volume of operations on resources using the RID identifier that result in 429s (as opposed to id property), these 429 will not appear when Metrics are filtered to the resource
    - To have these 429s appear in Metrics, use the id property when performing these operations

**Metadata throttling**

- Scenario: You are seeing high rate of throttling (429) in the **System** metrics tab, and want to know the cause:

    - Metadata throttling can occur when you are performing a high volume of CRUD operations on databases or containers, such as listing databases/containers or querying for offers to see the current provisioned throughput
    - Increasing the RU of the database or container will have no impact and is not recommended
    - Instead, identify which client is issuing these operations and consider implementing a backoff policy to send these requests at a lower rate

### **Cannot view my MongoDB API data**

* The Data Explorer uses the native SDK based on the Azure Cosmos DB Account API type to access the data from the service
* Using the Azure Cosmos DB SQL API SDK to perform CRUD operations against a MongoDB API account will not generate any errors. However, this would make the Data Explorer produce the internal server error when reading the data due to a mismatch in the data formats.
* Use the native MongoDB SDKs to perform CRUD operations against your Azure Cosmos DB MongoDB API account

### **Query results not as expected**

* By default, the Data Explorer returns query results in pages, with up to 100 results per page. To view additional pages of results, select the **"Load more"** button under the results tab. You can adjust the maximum number of results per page in the Data Explorer **Settings** tab. 

### **Unable to create account with notebooks, or enable notebooks on an existing account**

* Built-in notebooks for Azure Cosmos DB are currently available in the following Azure regions: Australia East, East US, East US 2, North Europe, South Central US, Southeast Asia, UK South, West Europe and West US 2. 
* To use notebooks, create a new account with notebooks or enable notebooks on an existing account in one of these regions.

## **Recommended Documents**

* Review [Get started with Azure Cosmos DB MongoDB API](https://docs.microsoft.com/azure/cosmos-db/mongodb-introduction#how-to-get-started) for building MongoDB API applications
* [Virtual Networks](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-vnet-service-endpoint)
* [Firewalls](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall)
* [Stored procedures, triggers, UDFs](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs)
* [Enable built-in notebooks](https://docs.microsoft.com/azure/cosmos-db/enable-notebooks)
* [How to use notebook features](https://docs.microsoft.com/azure/cosmos-db/use-notebook-features-and-commands)
