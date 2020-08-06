<properties
	pageTitle="Timeout while running Sync or CleanupTombstone"
	description="A timeout ocurred while running Sync or CleanupTombstone"
	infoBubbleText="A timeout ocurred while running Sync or CleanupTombstone"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_timeout_sync_or_cleanup_tombstone"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# Timeout while running Sync or CleanupTombstone

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
We were able to detect timeouts:<br>
**<!--$TimeoutRunningSyncOrCleanupTombstoneDatabaseList--> TimeoutRunningSyncOrCleanupTombstoneDatabaseList <!--/$TimeoutRunningSyncOrCleanupTombstoneDatabaseList-->**
<!--/issueDescription-->

## **Recommended Steps**

It's likely that indexes in your tables or in the data sync tracking tables got fragmented. Please check for index fragmentation in the database, **Reorganize or Rebuild Indexes** if needed, and try again. You may use the following query to identify the average fragmentation in percent:

```
SELECT '['+s.[name]+'].['+ t.[name]+']' as TableName
,i.[name] as [IndexName]
,CONVERT(DECIMAL(10,2),idxstats.avg_fragmentation_in_percent) as FragmentationPercent
,idxstats.page_count AS [PageCount]
FROM sys.dm_db_index_physical_stats (DB_ID(), NULL, NULL, NULL, NULL) AS idxstats
INNER JOIN sys.tables t on t.[object_id] = idxstats.[object_id]
INNER JOIN sys.schemas s on t.[schema_id] = s.[schema_id]
INNER JOIN sys.indexes AS i ON i.[object_id] = idxstats.[object_id] AND idxstats.index_id = i.index_id
WHERE idxstats.database_id = DB_ID() AND idxstats.avg_fragmentation_in_percent >= 5
ORDER BY idxstats.avg_fragmentation_in_percent desc
```

You can find how to reorganize or rebuild a fragmented index in SQL Server at [Reorganize and Rebuild Indexes](https://docs.microsoft.com/sql/relational-databases/indexes/reorganize-and-rebuild-indexes).
