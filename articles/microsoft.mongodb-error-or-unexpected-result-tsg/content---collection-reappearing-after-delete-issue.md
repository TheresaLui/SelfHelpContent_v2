<properties
	pageTitle="Collection Reappearing after delete issue"
	description="Collection Reappearing after delete issue"
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
	articleId="33564244-70ba-47be-8332-6f9b83d04189_content"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Collection Reappearing after delete issue

The Request5m does confirm the delete and create. **Note:** The create and Delete through portal is shown in the Reques5M.
Incase, the create and delete is performed through shell or using mongo sdk, the MongoProxyRequest5M should show the command "Create"

~~~kusto

Request5M
| where globalDatabaseAccountName  =="ACCOUNTNAME" //and CollectionRid =="COLLECTIONRID"
| where TIMESTAMP >= datetime(2020-05-28 09:50:00.0000000)
| where TIMESTAMP <= datetime(2020-05-28 09:55:00.0000000)
| where verb  !in('GET','OPTIONS')
| project TIMESTAMP, category, verb, statusCode, subStatusCode, offerThroughput, userAgent

~~~

The above data show the userAgent used to perform the delete and create. Note The Post is the creation operation.

Run  below query to find the operation performed during the timeframe. Since **the mongo wire portal states that an insert against a non existing collection would trigger creating the collection.**
```
MongoProxyRequest5M
| where DatabaseAccountName contains "ACCOUNTNAME"  and CollectionName =="COLLECTIONNAME"
| where TIMESTAMP >= datetime(2020-05-28 09:50:00.0000000)
| where TIMESTAMP <= datetime(2020-05-28 09:55:00.0000000)
| project TIMESTAMP, CommandName, DatabaseAccountName, DatabaseName, CollectionName, ClientInformation
```

The MongoProxyRequest5M does show the create collection
```
MongoProxyRequest5M
| where DatabaseAccountName =="ACCOUNTNAME" and TIMESTAMP > ago(1d)
| project TIMESTAMP, CommandName,  DatabaseAccountName, CollectionName, ClientInformation| where CommandName == "create"
```

Using the UserAgent you can find which application performed the delete/create Using the MongoProxy for mongo collection to validate the Command column value "insert". If so then the insert does auto create the collection.
