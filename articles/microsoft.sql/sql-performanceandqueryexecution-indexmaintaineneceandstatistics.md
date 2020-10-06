<properties
	pageTitle="Resolve index and statistics related issues in Azure SQL Database"
	description="Resolve index and statistics related issues in Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32749517"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    	resourceTags="servers, databases"
	articleId="sql-performanceandqueryexecution-indexmaintaineneceandstatstics"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve index and statistics related issues in Azure SQL Database

Up-to-date index statistics are crucial for the SQL DB query optimizer to generate optimal execution plans. Better execution plans use the right amount of resources and improve's performance , thus the first place to start is by updating statistics.

### **Updating statistics**

SQL Server automatically updates statistics on tables with more than 500 records, and that have over 20% of the rows modified. When the amount of change does not cross this 20% threshold the statistics are outdated, leading to bad cardinality estimation and bad query execution plans. You can update statistics using the query below:

```
-- This will update all the statistics on all the tables in your database.
-- remove the comments from EXEC sp_executesql in order to have the commands actually update stats, instead of just printing them.

SET NOCOUNT ON
GO

DECLARE updatestats CURSOR FOR
SELECT table_schema, table_name 
FROM information_schema.tables
where TABLE_TYPE = 'BASE TABLE'
OPEN updatestats

DECLARE @tableSchema NVARCHAR(128)
DECLARE @tableName NVARCHAR(128)
DECLARE @Statement NVARCHAR(300)

FETCH NEXT FROM updatestats INTO @tableSchema, @tableName
WHILE (@@FETCH_STATUS = 0)
BEGIN
SET @Statement = 'UPDATE STATISTICS '  + '[' + @tableSchema + ']' + '.' + '[' + @tableName + ']' + '  WITH FULLSCAN'
PRINT @Statement -- comment this print statement to prevent it from printing whenever you are ready to execute the command below.

--EXEC sp_executesql @Statement -- remove the comment on the beginning of this line to run the commands

FETCH NEXT FROM updatestats INTO @tableSchema, @tableName
END

CLOSE updatestats
DEALLOCATE updatestats

GO
SET NOCOUNT OFF
GO

```


### **Using automation** 

You can use Azure Automation to run a scheduled runbook that can do the index and statistics maintenance for you. To configure the same, please follow [Automating Azure SQL DB index and statistics maintenance using Azure Automation](https://techcommunity.microsoft.com/t5/azure-database-support-blog/automating-azure-sql-db-index-and-statistics-maintenance-using/ba-p/368974).

### **Guidelines for creating\updating large indexes**

If you are creating\updating a large index please follow the following [guidelines](https://docs.microsoft.com/sql/relational-databases/indexes/guidelines-for-online-index-operations?view=sql-server-2017).

## **Recommended Documents**

* [Indexes](https://docs.microsoft.com/sql/relational-databases/indexes/indexes?view=sql-server-2017)
* [Adaptive index defragmentation](https://github.com/Microsoft/tigertoolbox/tree/master/AdaptiveIndexDefrag)
* [How to maintain Azure SQL Indexes and Statistics](https://techcommunity.microsoft.com/t5/azure-database-support-blog/how-to-maintain-azure-sql-indexes-and-statistics/ba-p/368787)

