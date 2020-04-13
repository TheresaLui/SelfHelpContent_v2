<properties
	pageTitle="Unsupported object names in Data Sync"
	description="Unsupported object names in Data Sync"
	infoBubbleText="Found unsupported object names in Data Sync"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_invalidobjectnames"
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
In Data Sync, the names of objects (databases, tables, and columns) cannot contain the printable characters period (.), left square bracket ([), or right square bracket (]).<br>

We were able to detect unsupported object names in the Database(s):<br>
**<!--$InvalidObjectNamesDatabaseList--> InvalidObjectNamesDatabaseList <!--/$InvalidObjectNamesDatabaseList-->**
<!--/issueDescription-->

## **Recommended Steps**

You may use the following query to identify tables and/or columns with unsupported characters and rename them:

```
SELECT table_schema, table_name, column_name 
FROM   information_schema.columns 
WHERE  table_name LIKE '%.%' 
OR table_name LIKE '%[[]%' 
OR table_name LIKE '%]%' 
OR column_name LIKE '%.%' 
OR column_name LIKE '%[[]%' 
OR column_name LIKE '%]%'
```

Data Sync schema can be set from any database. Alternatively, you can:

1. Create the tables you want to sync in another database of the sync group that does not have unsupported characters (if not created already)
2. "Refresh Schema" from that other database
3. Select the tables and save
4. Trigger "Sync"
