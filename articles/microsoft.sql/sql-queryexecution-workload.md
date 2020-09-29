<properties
    pageTitle="query execution/increased workload"
    description="query execution/increased workload"
    infoBubbleText="Found increased worload issues with DB. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="pxding"
    ms.author="pedin"
    displayOrder=""
    articleId="IsWorkLoadIssue_WL112688-E6C3-1004-B3D3-188FD8FC30EA"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32630434,32630450,32630454,32630459"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# We ran diagnostics on your resource and found Increased Workload

<!--issueDescription-->
Our internal service telemetry detected that over the past 24 hours there has been a significant increase (50% or more) in user requests on your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** in server **<!--$ServerName-->ServerName<!--/$ServerName-->**.
<!--/issueDescription-->

## **Recommended Steps**

This user load increase is potentially contributing to performance issues or timeouts due to lack of resources to execute the requested workload during that specific period. Please consider upgrading your database SLO, tuning your queries, or balancing your workload. Please see the recommended articles for more details. 

## **Recommended Documents**

* [Use Query performance insights to identify the queries which are causing the high CPU consumption](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance)
* [Enable Automatic tuning provides peak performance and stable workloads through continuous performance tuning utilizing Artificial Intelligence](https://docs.microsoft.com/azure/sql-database/sql-database-automatic-tuning)
* [Increase Azure Database tier to get more DTUs and hence accommodate for more workload in your environment](https://azure.microsoft.com/pricing/details/sql-database/single)
* [If the workload is varying, then consider moving few databases into SQL elastic pool to share DTUs](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
