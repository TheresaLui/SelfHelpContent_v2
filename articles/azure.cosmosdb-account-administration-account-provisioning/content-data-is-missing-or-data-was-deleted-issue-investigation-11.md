<properties
	  pageTitle="Data is missing or data was deleted issue investigation"
	  description="Data is missing or data was deleted issue investigation"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="ec531613-2120-4a61-b02b-7274fbdbc2b1"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Data is missing or data was deleted issue investigation

The documents in the collection might be removed in the following cases.

* The application called the delete operation
* The application deleted the collection and recreated the collection.
* The TTL configuration was set and the TTL triggered the archival process.

**Application called the delete operation**  
* The backendEndRequest5m should be able to provide that the delete was performed by the application.

```
BackendEndRequest5M
| where  GlobalDatabaseAccountName =="fastertable" and TIMESTAMP  > ago (3h) and OperationType ==4 and ResourceType ==2
| summarize sum(SampleCount) by OperationType , ResourceType , StatusCode, UserAgent
```

* The User or Application deleted the collection and recreated the collection.
Please refer to the
[TSG Admin: Collection /Database Delete Auditing or How to find who Delete my Collection or Database](https://supportability.visualstudio.com/AzureCosmosDB/_wiki/wikis/AzureCosmosDB.wiki/237003)

* The Application or User configured the TTL and TTL Archived the data. The TTL configuration is a collection Replace operation which is logged in the BackendEndRequest5m.

```
BackendEndRequest5M
| where  GlobalDatabaseAccountName =="fastertable" and TIMESTAMP  > ago (1d) and OperationType ==5 and ResourceType ==1
| summarize sum(SampleCount) by OperationType , ResourceType , StatusCode, UserAgent, CollectionRid
```

