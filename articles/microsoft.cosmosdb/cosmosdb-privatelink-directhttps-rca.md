<properties
    pageTitle="Direct Mode TCP recommendation for Private Link accounts RCA"
    description="RCA - Private Link customer recommended to use Direct Mode TCP"
    infoBubbleText="The customer is recommended to use Direct Mode TCP to use Private Link"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-privatelink-directhttps-rca"
    diagnosticScenario="CosmosDBPrivateLinkDirectHTTPSInsight"
    selfHelpType="rca"
    supportTopicIds="32738664, 32738665"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Upgrade to MongoDB API engine version 3.6

## As an Azure Private Link customer, we recommend that you use Direct Mode with TCP instead of HTTPS

<!--issueDescription-->
Direct Mode with HTTPS is not compatible with Azure Private Link. However, using Direct Mode with TCP will allow you to use Azure Private Link and all its great features.

<!--/issueDescription-->

## **Recommended Documents**

- [Azure Cosmos DB's API for MongoDB (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
