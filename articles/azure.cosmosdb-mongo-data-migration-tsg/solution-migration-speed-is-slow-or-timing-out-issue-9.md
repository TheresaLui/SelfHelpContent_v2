<properties
	  pageTitle="Migration Speed is Slow or Timing Out issue"
	  description="Migration Speed is Slow or Timing Out issue"
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
	  articleId="d9ea877e-8ceb-4755-8cc4-d463347d3c25"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Migration Speed is Slow or Timing Out issue

<!--issueDescription-->

Dear customer,

If you are getting a slow migration speed please follow the steps below.

###Solution 
Regarding restore speed - the Cosmos DB API works most efficiently with multiple workers.  
Please try having them use --numInsertionWorkers with a number greater than 1 to see if that allows a higher throughput.

Please see: https://docs.microsoft.com/en-us/azure/dms/tutorial-mongodb-cosmos-db?toc=/azure/cosmos-db/toc.json  
And Command reference:  https://docs.mongodb.com/manual/reference/program/mongorestore/index.html


If you doen't want to use ADF and would like to use MongoRestore command please follow the below steps.
- Before you start migrating we recommend you to pre-create your collections with high number of RU/s  in the first place and once the migration is done you can scale down the RU/s.
- You also need to provide the Batchsize and numInsertionWorkers property while running the mongorestore command as shown below.

` 
mongorestore.exe -- <your_hostname>:10255 -u <your_username> -p <your_password> --db <your_database> --ssl --sslAllowInvalidCertificates <path_to_backup> --numInsertionWorkersPerCollection 1 --batchSize 24
`


##Please follow the below steps to calculate the batch size and NuminsertionWorkers.

1. Calculate the approximate RU charge for a single document write  
Connect to Azure Cosmos DB Mongo DB database from the Mongo DB Shell and run a simple insert command as shown below (Below document is a sample one. Please insert any document of yours)
 
```
globaldb:PRIMARY> db.coll.insert({"_id":"224n5dHRLNjhzovwH","createdAt":{"$date":"2018-05-13T17:33:52.897Z roles":{"typeOfUser":["user"]}})
```
 
Run db.runCommand({getLastRequestStatistics:1}) as shown below and take note of request charge
 
```
globaldb:PRIMARY> db.runCommand({getLastRequestStatistics: 1})
{
        "_t" : "GetRequestStatisticsResponse",
        "ok" : 1,
        "CommandName" : "insert",
        "RequestCharge" : 48,
        "RequestDurationInMilliSeconds" : NumberLong(1305)
}
```


2. Determine the latency from your machine to the Azure Cosmos DB cloud service by following the below steps:
```
setVerboseShell(true)    
Run db.coll.find().limit(1)
```

```
globaldb:PRIMARY> db.coll.find().limit(1)
{ "_id" : "224n5dHRLNjhzovwH", "createdAt" : { "$date" : "2018-05-13T17:33:52.897Z" }, "roles" : { "typeOfUser" : [ "user" ] } }
Fetched 1 record(s) in 48ms
```


3.  Calculate the batchSize and numinsertionworkers values
- For batchSize, divide the total provisioned RUs by the RUs consumed from your single document write in step 1.
- If the calculated batchSize <= 24, use that number as your batchSize value.
- If the calculated batchSize > 24, set the batchSize value to 24.
- For numInsertionWorkers, use this equation: numInsertionWorkers = (provisioned throughput * latency in seconds) / (batch size * consumed RUs for a single write).



| Property | Value |
|--|--|
| batchSize | 24 |
| RUs provisioned | 10000  |
| Latency | 0.048 s |
|RU charged for 1 doc write  | 48 RUs |
| numInsertionWorkers | 1 |

numInsertionWorkers = (10000 RUs x 0.048 s) / (24 x 48 RUs) = 0.41

<br>
<br>

4. Run the Migration command

`
mongorestore.exe -- <your_hostname>:10255 -u <your_username> -p <your_password> --db <your_database> --ssl --sslAllowInvalidCertificates <path_to_backup> --numInsertionWorkersPerCollection 1 --batchSize 24
`

Thank you.

<!--/issueDescription-->

