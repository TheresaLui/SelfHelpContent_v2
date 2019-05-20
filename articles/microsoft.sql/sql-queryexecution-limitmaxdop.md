<properties
    pageTitle="query execution/high degree of MAXDOP"
    description="query execution/high degree of MAXDOP"
    infoBubbleText="Found high degree of MAXDOP with DB. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="pxding"
    ms.author="pedin"
    displayOrder=""
    articleId="RequestLimit_6191C0C8-FEBE-4C34-80E9-9F1FABC2A1A6"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32630450,32630459"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake"
/>

# We ran diagnostics on your resource and found high degree of MAXDOP

<!--/issueDescription-->

Our internal service telemetry detected that your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** in server **<!--$ServerName-->ServerName<!--/$ServerName-->** is an instance with high degree of MAXDOP. 

While using a higher degree of parallelism may increase throughput for individual queries, it can negatively impact concurrency in some workloads.

<!--/issueDescription-->

## **Recommended Documents**

* [Tune Azure SQL MaxDOP setting with Alter Database](https://docs.microsoft.com/sql/t-sql/statements/alter-database-scoped-configuration-transact-sql?view=sql-server-2017)
