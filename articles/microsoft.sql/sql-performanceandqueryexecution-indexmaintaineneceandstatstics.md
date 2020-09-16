<properties
	pageTitle="Resolve index and statistics related issues in Azure SQL Database"
	description="Resolve index and statistics related issues in Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32749515"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    	resourceTags="servers, databases"
	articleId="sql-performanceandqueryexecution-indexmaintaineneceandstatstics"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve index and statistics related issues in Azure SQL Database

Statistics are crucial for SQL engine to know how much data it will be working with and with that information creating better execution plans. Having better execution plans, queries will have better performance and will use the right amount of resources required run, thus to improve performance the first place to start is updating statistics.

### **Updating statistics**

SQL Server automatically updates statistics on tables with more than 500 records, and that have over 20% of the rows modified while the amount of change does not cross this 20% threshold, the statistics are outdated, leading to bad cardinality estimation, bad query execution plans. You can update statistics using the query below:

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

-- after updating statistics clear database procedure cache for the database to force the creation on new, more accurate execution plans

ALTER DATABASE SCOPED CONFIGURATION CLEAR PROCEDURE_CACHE

-- check available plans

select * from sys.dm_exec_cached_plans
```


### **Using automation** 

You can use Azure Automation to run a scheduled runbook that can do the index and statistics maintenance for you. To configure the same, please follow [Automating Azure SQL DB index and statistics maintenance using [Azure Automation](https://techcommunity.microsoft.com/t5/azure-database-support-blog/automating-azure-sql-db-index-and-statistics-maintenance-using/ba-p/368974)

### **Guidelines for creating\updating large indexes**

If you are creating\updating a large index please follow the following [guidelines](https://docs.microsoft.com/sql/relational-databases/indexes/guidelines-for-online-index-operations?view=sql-server-2017)

## **Recommended Documents**

* [Indexes](https://docs.microsoft.com/sql/relational-databases/indexes/indexes?view=sql-server-2017).
* [Adaptive index defragmentation](https://github.com/Microsoft/tigertoolbox/tree/master/AdaptiveIndexDefrag)
* [How to maintain Azure SQL Indexes and Statistics](https://techcommunity.microsoft.com/t5/azure-database-support-blog/how-to-maintain-azure-sql-indexes-and-statistics/ba-p/368787)

