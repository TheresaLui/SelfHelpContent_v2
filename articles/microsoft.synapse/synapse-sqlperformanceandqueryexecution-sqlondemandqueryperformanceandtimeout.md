<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "workspaces"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738810"
	displayOrder = ""
	diagnosticScenario = ""
	pageTitle = "SQL Performance and Query Execution/SQL on-demand query performance and timeout"
	description = "SQL Performance and Query Execution/SQL on-demand query performance and timeout"
	infoBubbleText = ""
	articleId = "synapse-sqlperformanceandqueryexecution-sqlondemandqueryperformanceandtimeout"
	authors = "saltug"
	ms.author = "fipopovi, saltug"
/>

# SQL Performance and Query Execution/SQL on-demand query performance and timeout

## **Recommended Steps**

* Visit [performance best practices for SQL on-demand](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/best-practices-sql-on-demand?branch=release-ignite-arcadia) to optimize your query.

* [Use fileinfo and filepath functions to target specific partitions](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/best-practices-sql-on-demand?branch=release-ignite-arcadia#use-fileinfo-and-filepath-functions-to-target-specific-partitions).

* Convert files to Parquet before querying.

* Partition your data into folders before querying.

* If your query targets CSV files, consider [creating statistics](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/development-tables-statistics?branch=release-ignite-arcadia#statistics-in-sql-on-demand-preview).

* Make sure you target storage accounts in the same region as your endpoint for optimal performance. You can find storage account and workspace regions on Azure Portal, in Overview blades of your storage account and workspace.

* If your query fails with the error message ?Distributed query timeout expired. The timeout period elapsed prior to completion of the distributed operation.?, it means that query lasted longer that allowed. Visit [performance best practices for SQL on-demand](https://review.docs.microsoft.com/azure/synapse-analytics/sql-analytics/best-practices-sql-on-demand?branch=release-ignite-arcadia) to optimize your query to execute faster.

