<properties
	pageTitle="Unsupported object names in Data Sync"
	description="Unsupported object names in Data Sync"
	infoBubbleText="Found unsupported object names in Data Sync"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_snapshotisolationdisabled"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# Unsupported object names in Data Sync

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
We were able to detect that snapshot isolation is disabled in the Database(s):<br>
**<!--$SnapshotIsolationDisabledDatabaseList--> SnapshotIsolationDisabledDatabaseList <!--/$SnapshotIsolationDisabledDatabaseList-->**
<!--/issueDescription-->

Snapshot isolation must be enabled. For more info, see [Snapshot Isolation in SQL Server](https://docs.microsoft.com/dotnet/framework/data/adonet/sql/snapshot-isolation-in-sql-server).

## **Recommended Steps**  

1. Connect to the database and enable snapshot isolation by running the following command:

```
ALTER DATABASE CURRENT SET ALLOW_SNAPSHOT_ISOLATION ON
```

You may now retry the operation, or wait for it to be automatically triggered by Data Sync (if applicable).
