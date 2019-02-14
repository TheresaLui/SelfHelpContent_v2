<properties
    pageTitle="query execution/increased workload"
    description="query execution/increased workload"
    infoBubbleText="Found increased worload issuse with DB. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="pxding"
    ms.author="pedin"
    displayOrder=""
    articleId="IsWorkLoadIssue_WL112688-E6C3-1004-B3D3-188FD8FC30EA"
    diagnosticScenario="dbasc"
    selfHelpType="rca"
    supportTopicIds=""
    resourceTags="databases, servers"
    productPesIds=""
    cloudEnvironments="public"
/>

# Query Execution/Increased Workload

## **Recommended Steps**

Our internal service telemetry detected that over the past 24 hours there has been a significant increase in user requests for your Azure SQL DB database. This user load increase is potentially contributing to performance issues or timeouts due to lack of resources to execute the requested workload during that specific period. Please go through following documents to troubleshoot and resolve this issue.

## **Recommended Documents**

* [Use Query performance insights to identify the queries which are causing the high CPU consumption](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance)
* [Enable Automatic tuning provides peak performance and stable workloads through continuous performance tuning utilizing Artificial Intelligence](https://docs.microsoft.com/azure/sql-database/sql-database-automatic-tuning)
* [Increase Azure Database tier to get more DTUs and hence accommodate for more workload in your environment](https://azure.microsoft.com/pricing/details/sql-database/single)
* [If the workload is varying, then consider moving few databases into SQL elastic pool to share DTUs](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
