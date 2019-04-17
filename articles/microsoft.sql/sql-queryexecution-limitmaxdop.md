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
    diagnosticScenario="dbasc"
    selfHelpType="rca"
    supportTopicIds="32630434,32630459"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public"
/>

# Query Execution/high degree of MAXDOP

## **Recommended Steps**

Our internal service telemetry detected that {DatabaseName} is an instance of Azure SQL with a high degree of MAXDOP. While using a higher degree of parallelism may increase throughput for individual queries, it can negatively impact concurrency in some workloads.

## **Recommended Documents**

* [Tune Azure SQL MaxDOP setting with Alter Database](https://docs.microsoft.com/sql/t-sql/statements/alter-database-scoped-configuration-transact-sql?view=sql-server-2017)
