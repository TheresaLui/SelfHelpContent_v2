<properties
    pageTitle="Lazy Indexing detected"
    description="Lazy Indexing RCA"
    infoBubbleText="Customer has one or more containers using Lazy indexing.. See the details on the right."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="andresferreira"
    ms.author="anferrei"
    articleId="cosmosdb-lazyindexing-rca"
    diagnosticScenario="LazyIndexingInsight"
    selfHelpType="rca"
    supportTopicIds="32636761,32675640,32684529,32741533,32636754,32636818,32636795,32636821,32741534,32636755,32636768,32636802,32681012"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Lazy Indexing detected

## We ran diagnostics on your account **<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->** and found an issue

<!--issueDescription-->
We found one or more containers using Lazy indexing. You should consider using **consistent** index and stop using **lazy** indexing.
<!--/issueDescription-->

## **Recommended Steps**

We highly recommend upgrading to **consistent** index for performance and reliability improvements. Lazy indexing performs updates to the index at a much lower priority level when the engine is not doing any other work. This can result in **inconsistent or incomplete** query results. If you plan to query a Cosmos container, you should not select lazy indexing. 

For consistent and optimal query performance, we recommend selecting **consistent indexing**. The RU charge for the same query will be significantly lower in a container with **consistent indexing** than a container with lazy indexing. In addition, many indexing features such as composite indexes require **consistent indexing**.  

Because the benefits of **consistent indexing** are significant, we have removed the option for lazy indexing in new containers. We want to encourage customers to follow this indexing best practice.

## **Recommended Documents**
[Indexing Mode](https://docs.microsoft.com/azure/cosmos-db/index-policy#indexing-mode)
