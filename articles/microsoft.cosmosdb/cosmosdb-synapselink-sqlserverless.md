<properties
	pageTitle="Azure Synapse Link for Cosmos DB - sqlserverless"
	description="Azure Synapse Link for Cosmos DB - sqlserverless"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32742615"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-sqlserverless"
	displayOrder="314"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>


# FAQ for Azure Synapse Link for Azure Cosmos DB - SQL Serverless

Most users can resolve issues in Azure Synapse Link for Azure Cosmos DB by applying the following answers to frequently asked questions.

## **Recommended Steps**  

### **Supported APIs**

Currently, Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview. For more information, contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.

### **Why is my query not showing the data I just inserted into Azure Cosmos DB Container?**

- Azure Cosmos DB syncs your transactional data with the analytical store within five minutes. Wait up to five minutes, and then rerun your query.
- Do not set your transactional TTL to less than two minutes because the data will be archived before the analytical store sync job runs. For data volumes that are smaller than 500 MB/minute, use transactional TTL that's greater than five minutes.

### **Why is my query not working for the Linked Service for Azure Cosmos DB that I created?**
- Support for Linked Services is planned for the first half of 2021. Until then, use the `OPENROWSET` function.
- Try using Linked Services for Azure Cosmos DB containers by having the analytical store enabled.

### **Can I load data into Cosmos DB by using SQL Serverless?**

No. Synapse SQL Serverless is read-only.

### **How do I fix an error that occurs when I try to create a view?**

- Use a user database to create a view. You can't use the **master** or the **default** databases to do this.
- If you try to create a view in the Synapse default database, you receive an "Operation CREATE/ALTER VIEW is not allowed for a replicated database" error message.
- If you try to create a view in the Synapse master database, you receive a "CREATE/ALTER VIEW is not supported in master database" error message.

### **Performance best practices**

Co-locate data and analytical workloads in the same Azure region. You can use the connection string to change from the primary region to any secondary region.

#### **When you use Synapse SQL serverless together with Power BI**
- Always check your tenant location
- Set up a cache for a better user experience
- Avoid returning millions of records to a dashboard
- Use scheduled refreshes. This helps you to avoid parallel queries execution that drain SQL Serverless pool resources.

- You can use Spark to pre-aggregate common analytical queries. This *write once/read many* approach can avoid heavy queries that are run continuously.

- Joins between different data stores: Use filters to avoid big data volumes that were moved across your Azure infrastructure.

- Currently, only `Latin1_General_100_BIN2_UTF8` collation can push filters down. This avoids transferring all data from storage to Synapse.

- If you are casting/converting data to `char` or `varchar` in query time, use the most optimal size. When possible, avoid using `VARCHAR(MAX)`.

- Automatic inference converts datatypes to a format that may not be optimal. Use the WITH clause to optimize data types.

- Synapse SQL Serverless pool resources have limits. Queries that are run simultaneously consume resources simultaneously. It is common to see PBI dashboards reaching resource limits when multiple refreshes occur in parallel. Tests and scheduled refreshes can help you avoid this problem. Also, multiple Synapse workspaces can address greater concurrency requirements.

- After you create a view, you can query `sys.columns` for this view or use `sp_describe_first_result_set` and *select top 0 from view* to check the data types. This is faster than using `SELECT * FROM...`.

- Use the [Statement Generator](https://htmlpreview.github.io/?https://github.com/Azure-Samples/Synapse/blob/main/SQL/tools/cosmosdb/generate-openrowset.html) to automatically create optimum column formats for your query.

- You can use the `OPENJSON` function to expose nested JSON data as columns. But if you also use the `AS JSON` option, the column type must be `NVARCHAR(MAX)`. This is not ideal for performance. The best option is to use the `WITH` clause to expose nested arrays as columns.

- The Cosmos DB transactional store partition key is not used in the analytical store. In Synapse Link, you can now model your transactional data to optimize data ingestion and point reads.

## **Recommended Documents**

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>This article answers commonly-asked questions about Synapse Link for Azure Cosmos DB  

[Query Azure Cosmos DB data with serverless SQL pool in Azure Synapse Link](https://docs.microsoft.com/azure/synapse-analytics/sql/query-cosmos-db-analytical-store)
<br> This article has details and examples about Synapse SQL Serverless Pool for Synapse Link  
