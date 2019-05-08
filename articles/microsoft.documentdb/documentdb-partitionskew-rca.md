<properties
	pageTitle="Partition skew RCA"
	description="RCA - Highly skewed paritions found on collection"
	infoBubbleText="Highly skewed partitions detected for one of the collections. See details on the right"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathb"
	displayOrder=""
	articleId="partitionskew_81BCE04B-904A-4007-8689-1F0A46A97208"
  diagnosticScenario="MachineKeyUpdates"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We found that data is unevenly distributed across the partitions for one of the collections
<!--/issueDescription-->
Since the data is not distributed evenly across partitions for the collection, it is possible that the requests to the collections are skewed too. This might result in performance issues if the partition does not have enough throughput. Follow this [link](https://docs.microsoft.com/azure/cosmos-db/partition-data) to choose a different partition key to be able to evenly distribute the data
