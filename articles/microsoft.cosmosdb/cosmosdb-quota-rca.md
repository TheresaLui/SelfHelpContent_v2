<properties
    pageTitle="Collection quota full - RCA"
    description="RCA - Collection quota full"
    infoBubbleText="Found information related to Machine Key Status. See details on the right."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="bharathsreenivas"
    ms.author="bharathb"
    articleId="cosmosdb-quota-rca"
    diagnosticScenario="CosmosDBQuotaInsight"
    selfHelpType="rca"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Collection quota full

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We found that your collection has reached its storage limit.
<!--/issueDescription-->

## **Recommended Steps**

It appears that you have reached the storage limit for your fixed collection. You will not be able to add more data into this collection. Please migrate the data into a partitioned collection to avoid hitting quota issues.
