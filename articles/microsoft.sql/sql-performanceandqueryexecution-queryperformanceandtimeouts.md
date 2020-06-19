<properties
	pageTitle="Resolve poor performance and timeout issues in Azure SQL Database"
	description="Resolve poor performance and timeout issues in Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa,andikshi"
  ms.author="emlisa,andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32630450"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
	articleId="e7df013f-4ee6-41d4-9e8f-f2f99692a25b"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve poor performance and timeout issues in Azure SQL Database

## TempDB Issues

If you are facing issues due to Tempdb being full, and are not able to resolve it, you can do a failover to clear tempdb. 
Failover changes the node of a database and moves it to a new node, it is recommended that you do not have any active workload running if you are doing a failover. 

<a href="https://docs.microsoft.com/rest/api/sql/databases(failover)/failover">Failover Rest API</a> can be used to easily failover your Azure SQL database to a new node.


## **Recommended Steps**

* Poor performance in Azure SQL DB is most often either related to excessive CPU utilization or a query waiting on a resource. To resolve either of these issues, review [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview?WT.mc_id=pid:13491:sid:32630450/).

