<properties
	pageTitle="Resolve poor performance and timeout issues in Azure SQL Database"
	description="Resolve poor performance and timeout issues in Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
  ms.author="emlisa"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32630450"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax"
    resourceTags="servers, databases"
	articleId="e7df013f-4ee6-41d4-9e8f-f2f99692a25b"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve poor performance and timeout issues in Azure SQL Database

## **Recommended Steps**

* Poor performance in Azure SQL DB is most often either related to excessive CPU utilization or a query waiting on a resource. To resolve either of these issues, review [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview?WT.mc_id=pid:13491:sid:32630450/).
* Another very common reason for poor performance is the lack of maintenance tasks to keep statistics up to date and preventing index fragmentation. You can use the [How to maintain Azure SQL Indexes and Statistics](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-maintain-Azure-SQL-Indexes-and-Statistics/ba-p/368787) solution to prevent this from happening.
