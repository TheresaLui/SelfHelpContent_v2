<properties
    pageTitle="query execution/high IO or high log rate usage"
    description="query execution/high IO or high log rate usage"
    infoBubbleText="Found high IO or high log rate usage issues with DB. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="pxding"
    ms.author="pedin"
    displayOrder=""
    articleId="HiIOUsageIssue_3EE4845D-971B-4A4B-9D1E-64D8C0B54ABB"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32630434,32630450,32630454,32630459"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Telemetry"
/>

# We ran diagnostics on your resource and found high IO or high log rate usage

<!--issueDescription-->
Our internal service telemetry detected high IO or high log rate usage greater than 90% for more than 5 consecutive minutes on your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** in server **<!--$ServerName-->ServerName<!--/$ServerName-->**.
<!--/issueDescription-->

## **Recommended Steps**

This indicates possible application slowness, timeouts due to lack of IO resources to execute the requested workload during that specific period. Please see the recommended articles for more details.

## **Recommended Documents**

* [Consider batching to reduce IO consumption when doing large operations](https://docs.microsoft.com/azure/sql-database/sql-database-use-batching-to-improve-performance)
* [Increase Azure Database tier to get more DTUs and hence accommodate for more IO in your environment](https://azure.microsoft.com/pricing/details/sql-database/single)
