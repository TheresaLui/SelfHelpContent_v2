<properties
    pageTitle="Direct Mode with TCP recommendation for Private Link accounts RCA"
    description="RCA - Private Link customer recommended to use Direct Mode with TCP"
    infoBubbleText="The customer is recommended to use Direct Mode with TCP to use Private Link"
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

# Use Direct Mode with TCP to connect to Azure Cosmos DB with Azure Private Link

## As an Azure Private Link customer, we recommend that you use Direct Mode with TCP instead of HTTPS

<!--issueDescription-->
Direct Mode with HTTPS is not compatible with Azure Private Link for Cosmos DB. However, using Direct Mode with TCP is completely supported. Please refer to [our Networking tips](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking) for guidance on how to use Direct Mode with TCP.

<!--/issueDescription-->

## **Recommended Documents**

- [Networking tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
- [Azure Private Link](https://docs.microsoft.com/azure/private-link/private-link-overview)
- [Azure Private Link for Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-private-endpoints)
