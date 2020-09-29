<properties
    pageTitle="Restricted Azure Capacity RCA"
    description="RCA - Restricted Azure Capacity"
    infoBubbleText="Restricted Azure Capacity. See details on the right."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="rnagpal"
    ms.author="rnagpal"
    articleId="cosmosdb-restricted-capacity-rca"
    diagnosticScenario="CosmosDBRestrictedCapacityInsight"
    selfHelpType="rca"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Capacity Restrictions (COVID-19)

We apologize for the inconvenience caused due to the capacity constraint. We currently have capacity constraints as the demand continues to grow due to ongoing COVID-19 situation.  

We have established clear criteria for the priority of new cloud capacity as documented in our [commitment to customers and Microsoft cloud services continuity](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/) and [Update #2 on Microsoft cloud services continuity](https://azure.microsoft.com/blog/update-2-on-microsoft-cloud-services-continuity/).  

As per the continuity plan, we have placed some restriction on your account for any new resource deployment and you may run into capacity constraints when performing the following operations:  

1. Provision/Create a new Cosmos DB Account(including Free-Tier account).
2. Adding a region to an existing Cosmos DB Account
3. Create a new database/container in an existing Cosmos DB Account which does not have any container yet.  

However, you should be able to perform all operations against your existing Azure Cosmos DB resources in all regions without any restrictions.  

Thank you for your ongoing trust in the Microsoft cloud to run your most critical workloads.

Please let us know for any questions or concerns.  

## **Recommended Steps**

If possible, please consider choosing any other region for new deployments which do not have any restrictions as of now.

## **Recommended Documents**

[Our commitment and service continuity](https://azure.microsoft.com/blog/update-2-on-microsoft-cloud-services-continuity/)
