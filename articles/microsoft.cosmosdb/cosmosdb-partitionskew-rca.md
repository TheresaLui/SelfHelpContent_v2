<properties
    pageTitle="Partition skew RCA"
    description="RCA - Highly skewed paritions found on collection"
    infoBubbleText="Highly skewed partitions detected for one of the collections. See details on the right"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="bharathsreenivas"
    ms.author="bharathb"
    articleId="cosmosdb-partitionskew-rca"
    diagnosticScenario="CosmosDBPartitionSkewInsight"
    selfHelpType="rca"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Highly skewed partitions detected on collection

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We found that data is unevenly distributed across the partitions for one of the collections
<!--/issueDescription-->

Since the data is not distributed evenly across partitions for the collection, it is possible that the requests to the collections are skewed too. This might result in performance issues if the partition does not have enough throughput.

## **Recommended Documents**

Follow this [link](https://docs.microsoft.com/azure/cosmos-db/partition-data) to choose a different partition key to be able to evenly distribute the data
