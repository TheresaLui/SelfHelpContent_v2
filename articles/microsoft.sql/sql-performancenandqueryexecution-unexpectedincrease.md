<properties
	pageTitle="performance and query execution/unexpected increase in resource consumption or DTUS"
	description="performance and query execution/unexpected increase in resource consumption or DTUS"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa,andikshi"
    ms.author="emlisa,andikshi"
    authorAlias="emlisa,andikshi"
	displayOrder="5"
	selfHelpType="generic"
	supportTopicIds="32630459"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="832be260-f5b8-47dc-95ba-288bcfc7625c"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# performance and query execution/unexpected increase in resource consumption or DTUS

## TempDB Issues

If you are facing issues due to Tempdb being full, and are not able to resolve it, you can do a failover to clear tempdb. 
Failover changes the node of a database and moves it to a new node, it is recommended that you do not have any active workload running if you are doing a failover. 

<a href="https://docs.microsoft.com/rest/api/sql/databases(failover)/failover">Failover Rest API</a> can be used to easily failover your Azure SQL database to a new node.

## **Recommended Documents**

* Descriptions of what happens when a database resource limit is reached for compute, storage, and sessions/workers limits, as well as corresponding mitigation steps can be found [here](https://docs.microsoft.com/azure/sql-database/sql-database-resource-limits-database-server#what-happens-when-database-resource-limits-are-reached?WT.mc_id=pid:13491:sid:32630459/)
* [Query Performance Insights](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance?WT.mc_id=pid:13491:sid:32630459/) can be used to easily monitor resource usage in your Azure SQL database (single or pooled database) by using build-in monitoring capabilities in the Azure portal <br>


