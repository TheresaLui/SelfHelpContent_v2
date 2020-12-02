<properties
    pageTitle="query execution/increased workload"
    description="query execution/increased workload"
    infoBubbleText="Increased customer workload detected. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="ketho00"
    ms.author="ketho"
    displayOrder=""
    articleId="IsWorkLoadIssue_WL112688-E6C3-1004-B3D3-188FD8FC30EA"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32749513,32749514,32749515,32749520"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Increase in User Workload

<!--issueDescription-->
We detected that over the past 2 hours there has been an increase in total user query executions on your database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->**. This database is using service tier **<!--$Slo-->Slo<!--/$Slo-->** and may not have enough resources to handle this user load increase.
<!--/issueDescription-->

## **Recommended Steps**
An increase in user workload is potentially contributing to performance issues or timeouts. 

To improve performance, follow these recommendations:
* To account for increased user workload, upgrade your database tier. For more information, go to [vCore and DTU purchasing models](https://docs.microsoft.com/azure/azure-sql/database/purchasing-models). 
* To help improve workload performance, enable [Automatic Tuning](https://docs.microsoft.com/azure/azure-sql/database/automatic-tuning-enable). 
* Identify and tune top resource consuming queries using [Query Performance Insights](https://docs.microsoft.com/azure/azure-sql/database/query-performance-insight-use).
* For a simple, cost-effective solution for managing and scaling multiple databases that have varying and unpredictable usage demands, move databases with volatile workloads into [Elastic Pools](https://docs.microsoft.com/azure/azure-sql/database/elastic-pool-overview). 
