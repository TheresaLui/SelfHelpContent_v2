<properties
	  pageTitle="Issue Category"
	  description="Issue Category"
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
	  articleId="207133f6-ef7a-4549-b1b1-5295440225dd"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Issue Category

The Azure Cosmos DB's API for MongoDB is compatible with MongoDB server version 3.6 by default for new accounts. See [MongoDB Feature Support (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36) for the list of supported operators and limitations.  

**Performance Investigation - Query and Collection information**

Run the following and capture the output:

- First run the customer query, eg: 
`db.<collectionName>.find(...<customer query params>...)`

- Immediately after the customer query, run:
`db.runCommand({getLastRequestStatistics:1})`

- Re-run the customer query with explain() added:
`db.<collectionName>.explain().find(...<customer query params>...))`

- Get collection information:
`db.runCommand({customAction:"GetCollection", collection:"<collectionName>", showIndexes:true})`

- Get index information:
`db.<collectionName>.getIndexes()`

You can also get:
- Number of documents in the collection
- Is the collection sharded  
  Note: If it is, then provide the shard key  
- Any other diagnostics

<br>
<br>
 
##How to fix it
Common Problems and Resolutions
- Inspect the explain results, indexes, and query to assure that all fields queried are indexed.
- Indexing all fields will improve performance and reduce RU consumption.
If the customer has a compound index covering the fields of the query, the compound index will not be used to serve requests outside of "sort". Please make sure that all fields are individually indexed.
- If any indexes return requresReIndex=true from the db.runCommand({customAction:"GetCollection", collection:"<collectionName>", showIndexes:true}) command, then follow the [Indexing TSG](https://supportability.visualstudio.com/AzureCosmosDB/_wiki/wikis/AzureCosmosDB.wiki/362602/TSG-Mongo-DB-Support-Known-Issues-3.6-?anchor=stuck-transaction-in-3.6).
- If the collection is sharded, make sure the shard key is indexed.
- If the collection is sharded and the query does not include the shard key, update the query to target a single shard.
- Upon inspecting the explain results, if there are any stages that take a great amount of time, try to reduce the number of documents that input to the stage.  This can be done by filtering more documents and aggregating earlier in the pipeline.
- If the query contains regex, note that regex is more intensive than simple equality so utilize $eq when possible.
- Review portal to check if the customer is getting 429s.  When server side retries are enabled, rate limiting will lead to increased latency or timeout exceptions.  Increase RUs as required.
- Review portal for hot partition.  If one exists consider new shard key.
- If none of these work, record the customer responses and results for all of the above and transfer to PG.

