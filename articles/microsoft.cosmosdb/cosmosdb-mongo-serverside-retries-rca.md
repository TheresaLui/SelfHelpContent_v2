<properties
    pageTitle="Enable server side retries for Azure Cosmos DB API for MongoDB account RCA"
    description="RCA - Enable server side retries for Azure Cosmos DB API for MongoDB account"
    infoBubbleText="The customer's account is eligible for server side retries"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-mongo-serverside-retries-rca"
    diagnosticScenario="CosmosDBMongoServerSideRetriesInsight"
    selfHelpType="rca"
    supportTopicIds="32636757"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Enable server side retries for the account

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The Cosmos DB account **<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->** is throwing a TooManyRequests error with the 16500 error code.
<!--/issueDescription-->

## Recommended Steps

We recommend [enabling server-side retries](https://docs.microsoft.com/azure/cosmos-db/prevent-rate-limiting-errors) on this account to mitigate the `TooManyRequests` issue. Note that server-side retries will prevent the service from ever sending a 16500 error. Instead, a request that would have resulted in a 16500 error will be delayed until sufficient RUs are available to complete the request, up to the request timeout of 60 seconds. Server-side retries work best when combined with autoscale.

Click [here](data-blade:Microsoft_Azure_DocumentDB.FeaturesBlade.id.$resourceId;data-blade-uri:{$domain}/#blade/Microsoft_Azure_DocumentDB/FeaturesBlade/id/{$resourceId}) to go to the Azure portal and enable server-side retries on your account.

## **Recommended Documents**

Learn more about [server-side retries](https://docs.microsoft.com/azure/cosmos-db/prevent-rate-limiting-errors)
