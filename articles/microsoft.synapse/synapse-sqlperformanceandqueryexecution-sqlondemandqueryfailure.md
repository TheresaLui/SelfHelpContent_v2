<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "workspaces"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738809"
	displayOrder = ""
	diagnosticScenario = ""
	pageTitle = "SQL Performance and Query Execution/SQL on-demand query failure"
	description = "SQL Performance and Query Execution/SQL on-demand query failure"
	infoBubbleText = ""
	articleId = "synapse-sqlperformanceandqueryexecution-sqlondemandqueryfailure"
	authors = "saltug"
	ms.author = "fipopovi, saltug"
/>

# SQL Performance and Query Execution/SQL on-demand query failure

## **Recommended Steps**

* If your query fails with the error message 'File cannot be opened because it does not exist or it is used by another process' and you're sure both file exist and it's not used by another process, it means SQL on-demand can't access the file 

	* If you are using AAD login, check whether UserIdentity credential exists. If it exists, check if you have proper rights to access the file. Easiest way is to grant yourself 'Storage Blob Data Contributor' role on the storage account you're trying to query. [Visit full guide on Azure Active Directory access control for storage for more information](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal). 
	* For credentials defined on storage path level, make sure credential is not created on storage level, but at least on container level 
	* For configuring storage access instructions, visit [control storage access for SQL on-demand](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control) 

* If your query fails with the error message 'The query references an object that is not supported in distributed processing mode.', it means that query targets data from both storage account and temporary table, which is not supported at this moment 

* If your query fails with the error message 'Operation is not allowed for a replicated database.', it means that query was executed in replicated database context. Replicated databases are automatically created as result of metadata synchronization with other Spark capabilities and are read-only. 

* If your query fails with the error message 'Distributed query timeout expired. The timeout period elapsed prior to completion of the distributed operation.', it means that query lasted longer that allowed. Visit [performance best practices for SQL on-demand](https://docs.microsoft.com/azure/synapse-analytics/sql/best-practices-sql-on-demand) to optimize your query to execute faster. 

* If your query fails with the error message 'This query cannot be executed due to current resource constraints.', it means that SQL OD is not able to execute it at this moment due to resource constraints: 

	* Please make sure data types of reasonable sizes are used. Also, specify schema for Parquet files for string columns as they will be VARCHAR(8000) by default. 
	* If your query targets CSV files, consider [creating statistics](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-tables-statistics#statistics-in-sql-on-demand-preview) 
	* Visit [performance best practices for SQL on-demand](https://docs.microsoft.com/azure/synapse-analytics/sql/best-practices-sql-on-demand) to optimize query 
