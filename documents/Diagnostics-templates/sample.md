<properties
    pageTitle="query execution/high degree of MAXDOP"
    description="query execution/high degree of MAXDOP"
    infoBubbleText="Found high degree of MAXDOP with DB. See details on the right."
    service="microsoft.sql"
    resource="servers"
    ms.author="msauthor"
    displayOrder=""
    articleId="newGuid"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="comma, seperated, list"
    resourceTags=""
    productPesIds="ProductId"
    cloudEnvironments="public,blackForest,fairfax,mooncake"
    ownershipId="CloudES_AzureSupportPlatform"
/>

# We ran diagnostics on your resource and found high request limit

<!--issueDescription-->
Our internal service telemetry detected that your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** in server **<!--$ServerName-->ServerName<!--/$ServerName-->** has reached the maximum request limit. Once the limit is reached, incoming requests are rejected until an ongoing request finishes.
<!--/issueDescription-->

## **Recommended Steps**

To resolve the issue, check if there are blocking queries. Blocking queries can use more requests than intended. You can also reduce MAXDOP for Premium instances or increase the database SLO for Standard instances.

## **Recommended Documents**

* [Finding Blocking Queries in Azure SQL DB](https://azure.microsoft.com/blog/finding-blocking-queries-in-sql-azure)
* [Tune Azure SQL MaxDOP setting with Alter Database](https://docs.microsoft.com/sql/t-sql/statements/alter-database-scoped-configuration-transact-sql?view=sql-server-2017)
* [Increase Azure Database tier to get more DTUs](https://azure.microsoft.com/pricing/details/sql-database/single)
