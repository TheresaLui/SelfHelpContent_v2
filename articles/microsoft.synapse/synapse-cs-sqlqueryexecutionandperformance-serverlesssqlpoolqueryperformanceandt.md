<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783910"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "SQL Query Execution and Performance/Serverless SQL pool - Query performance and timeout"
    description = "SQL Query Execution and Performance/Serverless SQL pool - Query performance and timeout"
    articleId = "synapse-cs-sqlqueryexecutionandperformance-serverlesssqlpoolqueryperformanceandt.md"
    ms.author = "fipopovi, saltug"
/>

# SQL Query Execution and Performance/Serverless SQL pool - Query performance and timeout

## **Recommended Steps**

* Visit [performance best practices for Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/best-practices-sql-on-demand) to optimize your query 

* [Use fileinfo and filepath functions to target specific partitions](https://docs.microsoft.com/azure/synapse-analytics/sql/best-practices-sql-on-demand#use-fileinfo-and-filepath-functions-to-target-specific-partitions) 

* Convert files to Parquet before querying 

* Partition your data into folders before querying 

* If your query targets CSV files, consider [creating statistics](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-tables-statistics#statistics-in-sql-on-demand-preview) 

* Make sure you target storage accounts in the same region as your endpoint for optimal performance. You can find storage account and workspace regions on Azure Portal, in Overview blades of your storage account and workspace. 

* If your query fails with the error message "Distributed query timeout expired. The timeout period elapsed prior to completion of the distributed operation.", it means that query lasted longer that allowed. Visit [performance best practices for Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/best-practices-sql-on-demand) to optimize your query to execute faster. 

 