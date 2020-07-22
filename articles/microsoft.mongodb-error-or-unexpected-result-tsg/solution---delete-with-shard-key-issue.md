<properties
	pageTitle="Delete with Shard Key issue"
	description="Delete with Shard Key issue"
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
	articleId="541fe7be-ca4b-46b2-b9e6-1c3817e0d339"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Delete with Shard Key issue

<!--issueDescription-->

Confirm customer is trying to delete some data in a CosmosDB and seeing an error as below:

**ERROR: Command delete failed: query in command must target a single shard key.**

We have tried both deleteMany() and remove() operations, both exhibit the same behaviour Our data has a GUID as the shard key, so we have 1.6million unique IDs

Provide customer with ready message below.

### Customer Message
Dear customer,

_deleteMany()_ and _remove()_ commands in MongoDB require a shardKey to be present. For your scenario, the recommended way is to delete documents in batches so that the delete request is not rate-limited and can fully utilize the provisioned throughput.

Below is a sample mongo shell snippet to delete documents in batches. Just replace query portion with the actual query and the limit portion with the number of documents to delete in a single batch. The snippet first gets the ids of all the documents to delete and then deletes then. For a sharded collection, the map function would need to change to return both the _id and the shardKey value

```
<script>
collection = 'testCollectionForBatchDelete';
limit = 100;
nRemoved = limit;
totalRemoved = 0;

for (i=0; nRemoved > 0; i++) {
    sleep(1000)
    print("Iteration " + i + ". Total documents removed: " + totalRemoved)
    idsToRemove = db.getCollection(collection).find({}, {_id:1}).limit(limit).toArray().map(function (d) { return d._id; })
    res = db.getCollection(collection).remove({_id: {$in: idsToRemove}})
    nRemoved = res.nRemoved
    totalRemoved = totalRemoved + nRemoved
}
db.getCollection(collection).count();
db.getCollection(collection).count();
</script>
```

Sample output:
```
globaldb:PRIMARY> limit = 500;
globaldb:PRIMARY> nRemoved = limit;
globaldb:PRIMARY> totalRemoved = 0;
globaldb:PRIMARY> for (i=0; nRemoved > 0; i++) {
... sleep(1000)  // Wait for a second before issuing next batch
... print("Iteration " + i + ". Total documents removed: " + totalRemoved)
... idsToRemove = db.getCollection(collection).find({}, {_id:1}).limit(limit).toArray().map(function (d) { return d._id; })
... res = db.getCollection(collection).remove({_id: {$in: idsToRemove}})
... nRemoved = res.nRemoved
... totalRemoved = totalRemoved + nRemoved
... }

Iteration 0. Total documents removed: 0
Iteration 1. Total documents removed: 500
Iteration 2. Total documents removed: 1000
Iteration 3. Total documents removed: 1500
Iteration 4. Total documents removed: 2000
```

You will need mongo shell (which ships as part of Mongo distribution) or any 3rd party mongo tool (like Robo3t, Mongo3t etc) to run the script.

<!--/issueDescription-->

