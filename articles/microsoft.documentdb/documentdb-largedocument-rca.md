<properties
	pageTitle="Large documents - RCA"
	description="RCA - High number operations inserting/updating large documents"
	infoBubbleText="High number operations inserting/updating large documents. See details on the right"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathb"
	displayOrder=""
	articleId="largedocument_2F574F61-4568-4D9D-940E-1817C22DC671"
  diagnosticScenario="MachineKeyUpdates"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We found a high number operations inserting/updating large documents
<!--/issueDescription-->
Inserting or updating large documents would require many RUs. If there are a large number of such operations, you might end up using most of your provisioned throughput. 

### Prefer smaller documents over larger documents
Writing a 1kb document = 5 RUs, 4kb document = 7 RUs, 64kb document = 48 RUs. Therefore, prefer smaller documents when possible. If your data can be subdivided into parts that are updated independently, consider breaking it up into smaller documents. 

Please see [Modeling 1-1, 1-N, and N-N for Cosmos DB](https://github.com/arramac/azure-documentdb-dotnet/tree/master/samples/Patterns/Patterns/03.ManyToMany)

### Evaluate encoding non-queryable content
If there are properties/sections in your items that are not queried, but need to be globally distributed or accessed at low latency, e.g. binary content or free text, consider an encoding/compression to reduce their footprint and RU consumption.

### Evaluate hybrid storage for binary content
If there are properties/sections in your items that are not queried, and do not need to be globally distributed or accessed at low latency, consider moving them out to Blob Storage and store just the reference along with indexable metadata in Cosmos DB items.

### For data skews, consider the salting pattern
If there are some keys with an uneven access pattern (e.g. super-users of your website who have a lot of activity events), consider the salting pattern so that their data can be spread across multiple partitions. See [Handling large partition keys](https://github.com/arramac/azure-documentdb-dotnet/tree/master/samples/Patterns/Patterns) for more details.

### Evaluate custom indexing policy
If your items are dense in content (contain a larege number of properties), the RUs consumed for indexing may be high. Every property consumes about 0.15 RUs, and this can add up if you have 100s-1000s or RUs. See [Indexing policies](https://docs.microsoft.com/azure/cosmos-db/indexing-policies) for more details.
