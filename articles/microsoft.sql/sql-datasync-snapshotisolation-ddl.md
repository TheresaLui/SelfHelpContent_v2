<properties
	pageTitle="Snapshot isolation transaction failed"
	description="Snapshot isolation transaction failed for the database"
	infoBubbleText="Snapshot isolation transaction failed for the database"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_snapshotisolation_ddl"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# Snapshot isolation transaction failed

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
Snapshot isolation transaction failed because the object accessed by the statement has been modified by a DDL statement in another concurrent transaction since the start of this transaction.  It is disallowed because the metadata is not versioned. A concurrent update to metadata can lead to inconsistency if mixed with snapshot isolation.<br>

We were able to detect snapshot isolation transaction failures in the Database(s):<br>

**<!--$SnapshotIsolationTransactionFailedDueToDDLDatabaseList--> SnapshotIsolationTransactionFailedDueToDDLDatabaseList <!--/$SnapshotIsolationTransactionFailedDueToDDLDatabaseList-->**

<!--/issueDescription-->

## **Recommended Steps**

This error can occur if you are querying metadata under snapshot isolation and there is a concurrent DDL statement that updates the metadata that is being accessed under snapshot isolation. SQL Server does not support versioning of metadata. For this reason, there are restrictions on what DDL operations can be performed within an explicit transaction running under snapshot isolation. An implicit transaction, by definition, is a single statement which makes it possible to enforce the semantics of snapshot isolation even with DDL statements. 

The following DDL statements are **not permitted** under snapshot isolation after a BEGIN TRANSACTION statement:

* ALTER TABLE
* CREATE INDEX
* CREATE XML INDEX
* ALTER INDEX
* DROP INDEX
* DBCC REINDEX
* ALTER PARTITION FUNCTION
* ALTER PARTITION SCHEME
* Any common language runtime (CLR) DDL statemen

These statements are permitted when you are using snapshot isolation within implicit transactions. An implicit transaction, by definition, is a single statement which makes it possible to enforce the semantics of snapshot isolation even with DDL statements.

Please avoid not permitted statements during a sync operation and try again.

## **Recommended Documents**

* [Snapshot Isolation in SQL Server](https://docs.microsoft.com/dotnet/framework/data/adonet/sql/snapshot-isolation-in-sql-server/)
