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
The Cosmos DB account **<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->** is being throttled a lot with the 16500 error code.
<!--/issueDescription-->

## Recommended Steps

It is recommended to enable server-side retries on this account to mitigate this issue.
