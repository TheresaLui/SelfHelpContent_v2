<properties
    pageTitle="Old SDK RCA"
    description="RCA - Old SDK"
    infoBubbleText="Old SDK detected for the account. See the details on the right."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-oldsdk-rca"
    diagnosticScenario="CosmosDBOldSDKInsight"
    selfHelpType="rca"
    supportTopicIds="32636763,32636796,32636801,32636775,32741535"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Old SDK detected

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->

Cosmos DB account **<!--$GlobalDatabaseAccountName-->GlobalDatabaseAccountName<!--/$GlobalDatabaseAccountName-->** has one or more client applications using version **<!--$SDKVersion-->SDKVersion<!--/$SDKVersion-->** of the **<!--$SDKType-->SDKType<!--/$SDKType-->** SDK that is an outdated version.

<!--/issueDescription-->

## **Recommended Steps**

* We highly recommend upgrading to the latest version of the SDK for performance and reliability improvements along with the latest bug fixes.

## **Recommended Documents**

* [Upgrade Cosmos DB <!--$SDKType-->SDKType<!--/$SDKType--> SDK](<!--$SDKReferenceUrl-->SDKReferenceUrl<!--/$SDKReferenceUrl-->)
