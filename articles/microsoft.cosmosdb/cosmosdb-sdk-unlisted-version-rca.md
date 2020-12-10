<properties
    pageTitle="Unlisted SDK version RCA"
    description="RCA - Unlisted SDK version"
    infoBubbleText="You're receiving this email because you currently use the Azure Cosmos DB .NET SDK version 3.14.0. See the details on the right."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="rnagpal"
    ms.author="rnagpal"
    articleId="cosmosdb-sdk-unlisted-version-rca"
    diagnosticScenario="CosmosDBUnlistedSDKInsight"
    selfHelpType="rca"
    supportTopicIds="32636818, 32783716, 32783724"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Unlisted version of SDK detected

## We ran diagnostics on your account **<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->** and found an issue

<!--issueDescription-->
We recently unlisted Azure Cosmos DB SQL API .NET SDK version 3.14.0 due to intermittent availability issues following a physical partition split. While most customers should not observe any issues, we recommend upgrading to Azure Cosmos DB .NET SDK version 3.15.0 or higher. 
<!--/issueDescription-->

## **Recommended Steps**

We recommend upgrading the SDK to at least version 3.15.0 to avoid this issue. 
For other SDKs (Java, Python, node.js) as well as .NET SDK versions older than 3.14, no action is needed.
