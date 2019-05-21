<properties
	pageTitle="Azure Cosmos DB about minimum RU"
	description="Azure Cosmos DB about minimum RU"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="kennthhz"
	ms.author="haozhag, padmaa"
	selfHelpType="generic"
	supportTopicIds="32636800"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-throughput-minru"
/>

# About minimum RU in Azure Cosmos DB

**How is minimum RU calculated?**

Azure Cosmos DB ensures that containers maintain minimum number of provisioned RUs based on the following factors:

* The maximum storage size that you ever used for the container.
* The maximum throughput that you ever provisioned for the container.
* The maximum number of Azure Cosmos containers that you ever created in a database with shared throughput.

Minimum throughput of the container can be found from the Portal or can be retrieved programmatically. Here is a sample .Net code to retrieve min throughput of the container 

```
  // Find the offer for the collection by SelfLink
  Offer offer = client.CreateOfferQuery(
      string.Format("SELECT * FROM offers o WHERE o.resource = '{0}'", collectionSelfLink)).AsEnumerable().FirstOrDefault();
  ResourceResponse<Offer> response = await client.ReadOfferAsync(offer.SelfLink);
  string minimumRUsForCollection = readResponse.Headers["x-ms-cosmos-min-throughput"];
```

The detailed description of how minimum RUs are calculated is based on the below formula:

Tmin = Max (Tmax / Kt , Smax * Ks,  Cmax * Kc, 400)

Tmax = Maximum throughput ever provisioned on the container or database
Smax = Maximum storage ever consumed on the container or database
Cmax = Maximum collection count ever created on a shared throughput database (For non-shared throughput, this is 0)

Kt = Throughput Scale coefficient = 60  
Ks = Storage Scale coefficient = 40 RU/GB. For collections created prior to Feb 2019, this value is 10 RU/GB.
Kc = Collection(s) Scale coefficient for shared throughput database = 100 RU/collection

## **Recommended Documents**

* [Request units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
* [Request unit calculator](https://www.documentdb.com/capacityplanner)
* [Set and get throughput for Azure Cosmos DB containers and database](https://docs.microsoft.com/azure/cosmos-db/set-throughput)
* [Partition and scale in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)
