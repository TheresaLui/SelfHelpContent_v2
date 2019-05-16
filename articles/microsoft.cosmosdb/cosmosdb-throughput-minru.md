<properties
	pageTitle="Azure Cosmos DB about minimum RU"
	description="Azure Cosmos DB about minimum RU"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="kennthhz"
	ms.author="haozhag, padmaa"
	selfHelpType="generic"
	supportTopicIds="32636761"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-throughput-minru"
/>

# About minimum RU in Cosmos DB

## **How is minimum RU calculated**

Cosmos DB ensures that containers maintain minimum amount of provisioned RUs based on the following factors:

* The maximum data size that you ever store in the container
* The maximum throughput that you ever provision on the container
* The maximum number of Azure Cosmos containers that you ever create in a database with shared throughput.

Minimum throughput of the container can be found from the Portal or can be retrieved programmatically. Here is a sample .Net code to retrieve min throughput of the container 

```
  // Find the offer for the collection by SelfLink
  Offer offer = client.CreateOfferQuery(
      string.Format("SELECT * FROM offers o WHERE o.resource = '{0}'", collectionSelfLink)).AsEnumerable().FirstOrDefault();
  ResourceResponse<Offer> response = await client.ReadOfferAsync(offer.SelfLink);
  string minimumRUsForCollection = readResponse.Headers["x-ms-cosmos-min-throughput"];
```

The detailed description of how minimum RUs are calculated is based on the below formula:

Tmin = Max (Tmax / Kt , Smax * Ks,  Cmax * Kc)

Tmax = Maximum throughput ever provisioned on the container or database
Smax = Maximum storage ever consumed on the container or database
Cmax = Maximum collection count ever created on a shared throughput database (For non-shared throughput, this is 0)

Kt = Throughput Scale co-efficient = 60  
Ks = Storage Scale co-efficient = 40 RU/GB. For collections created prior to Feb 2019, this value is 10 RU/GB.
Kc = Collection(s) Scale co-efficient for shared throughput database = 100 RU/collection

## **Recommended documents**

* [Request units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
* [Request unit calculator](https://www.documentdb.com/capacityplanner)
* [Set and get throughput for Azure Cosmos DB containers and database](https://docs.microsoft.com/azure/cosmos-db/set-throughput)
* [Partition and scale in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)