<properties
	pageTitle="Confirm if the collection was deleted successfully"
	description="Confirm if the collection was deleted successfully"
	service="Microsoft.DocumentDB"
	resource="databaseAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9eac36f7-bd5f-4fc0-b769-c2b492b100eb"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Confirm if the collection was deleted successfully

Customer asks why the collection is coming back some time after deleting the Mongo Collection.

Please collect the Database Name and the Collection Name. The below data  will show the Collection with different Collection RID along with the Min Start Time and Max End time. 
In case the Min Start and Max End time projects that same collection had different RID in the given time range, this proves the collection was deleted and got recreated.

```
ReportQuota5M
| where GlobalDatabaseAccountName =="GLOBALDABASEACCOUNTNAME" 
   and TIMESTAMP  > ago(3d) and DatabaseName =="DBNAME" 
   and CollectionName =="COLLECTIONNAME"
| summarize min(TIMESTAMP), max(TIMESTAMP) by GlobalDatabaseAccountName, DatabaseName, CollectionName, CollectionRid
```

The BackendEndRequest5M does confirms that the given collection was deleted through the operationtype ==4 (delete) and resource type ==1 (collection):
```
BackendEndRequest5M
| where GlobalDatabaseAccountName =="atera-mdb-us" and CollectionRid  =="cydQAORL9nE=" and OperationType ==4 and ResourceType ==1
| where TIMESTAMP >= datetime(2019-05-28 09:50:00.0000000)
| where TIMESTAMP <= datetime(2019-05-28 09:55:00.0000000)
| project TIMESTAMP, GlobalDatabaseAccountName, CollectionRid, OperationType, ResourceType
```

