<properties
	pageTitle="Azure Cosmos DB about long running scale operations"
	description="Azure Cosmos DB about long running scale operations"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="kennthhz"
	ms.author="haozhag, padmaa"
	selfHelpType="generic"
	supportTopicIds="32636798"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-throughput-longscaleoperation"
/>

# Azure Cosmos DB about long running scale operations

**How long will my scale operation take?**

Azure Cosmos DB currently only supports scale up operation. It is typically a long running operation. You can use below table to estimate how long it will take.

*Scale factor = New throughput/ Mininum throughput

| Min throughput        | Scale factor            | Estimated Duration  |
| --------------------- |:-----------------------:| -------------------:|
| 400                   | <25                     | <1 minute           |
| 400                   | 25 < Scale factor < 50  | 6 hours             |
| 400                   | 50 < Scale factor < 100 | 12 hours            |
| 400                   | 100 < Scale factor < 200| 18 hours            |
| >400                  | <100                    | <1 minute           |
| >400                  | 100 < Sacle factor < 200| 6 hours             |

## **Recommended documents**

* [Request units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
* [Request unit calculator](https://www.documentdb.com/capacityplanner)
* [Set and get throughput for Azure Cosmos DB containers and database](https://docs.microsoft.com/azure/cosmos-db/set-throughput)
* [Partition and scale in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)