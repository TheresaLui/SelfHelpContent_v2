<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783895"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Azure Synapse Link/My issue is not listed"
    description = "Azure Synapse Link/My issue is not listed"
    articleId = "synapse-cs-azuresynapselink-myissueisnotlisted.md"
    ms.author = "saltug"
/>

# Azure Synapse Link/My issue is not listed

Most users are able to resolve their Azure Synapse Link for Azure Cosmos DB issues using the steps below.  

## **Recommended Steps**  

### **Supported APIs**  

Today Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview. For more information, contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.  

### **Experiencing latency when adding a new Cosmos DB region**
For multi-region Azure Cosmos DB accounts, the data stored in the analytical store is also globally distributed. Regardless of single write region or multiple write regions, analytical queries performed from Azure Synapse Analytics can be served from the closest local region. 

If you're planning  to configure a multi-region Azure Cosmos DB account with analytical store support, we recommend having all the necessary regions added at time of account creation. If there are are large amounts of data, this can take a long time to complete.  

### **Picking a custom partitioning strategy for Analytical Store**
The data in analytical store is partitioned based on the horizontal partitioning of shards in the transactional store.  Currently, you cannot choose a different partitioning strategy for the analytical store.  

### **Synapse Link support for Azure Cosmos DB APIs**
In the public preview release, Synapse Link is supported only for Azure Cosmos DB SQL (Core) API and for MongoDB API. Support for Cassandra API is currently under gated preview.  To request access to gated preview, contact the Azure Cosmos DB Synapse Link at cosmosdbsynapselink@microsoft.com.  

### **Connecting to analytical store from analytics engines other than Azure Synapse Analytics**
You can only access and run queries against the analytical store using the various run-times provided by Azure Synapse Analytics. 
The analytical store can be queried and analyzed using:
* Synapse Spark with full support for Scala, Python, Spark SQL, and C#. Synapse Spark is central to data engineering and science scenarios 
* SQL serverless with T-SQL language and support for familiar BI tools (for example, Power BI Premium)  

### Is analytical store supported by Terraform?  

Currently Terraform doesn?t support analytical store containers. See [Terraform GitHub Issues](https://github.com/hashicorp/terraform/issues) for more information.  

## **Recommended Documents**  

[What is Azure Synapse Link for Azure Cosmos DB?](https://docs.microsoft.com/azure/cosmos-db/synapse-link)
<br> Synapse Link for Azure Cosmos DB  

[What is Azure Cosmos DB Analytical Store?](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview  

[Configure and use Azure Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link)
<br>Get started with Azure Synapse Link for Azure Cosmos DB  

[Azure Synapse Link for Azure Cosmos DB supported features](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/concept-synapse-link-cosmos-db-support)
<br>What is supported in Azure Synapse Analytics run time  

[Frequently asked questions about Azure Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>Frequently asked questions about Azure Synapse Link for Azure Cosmos DB  

[Azure Synapse Link for Azure Cosmos DB: Near real-time analytics use cases](https://docs.microsoft.com/azure/cosmos-db/synapse-link-use-cases)
<br>Azure Synapse Link for Azure Cosmos DB Use cases
 