<properties
    pageTitle="query execution/high IO usage"
    description="query execution/high IO usage"
    infoBubbleText="Found high IO usage issues with DB. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="pxding"
    ms.author="pedin"
    displayOrder=""
    articleId="HiIOUsageIssue_3EE4845D-971B-4A4B-9D1E-64D8C0B54ABB"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32630450,32630459"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake"
/>

# We ran diagnostics on your resource and found high IO usage

## **Recommended Steps**

Our internal service telemetry detected high IO usage greater than 90% for more than 5 consecutive minutes on {DatabaseName} during the period of {StartDateTime} UTC and {EndDateTime} UTC. This indicates possible application slowness, timeouts due to lack of IO resources to execute the requested workload during that specific period.

## **Recommended Documents**

* [Consider batching to reduce IO consumption when doing large operations](https://docs.microsoft.com/azure/sql-database/sql-database-use-batching-to-improve-performance)
* [Increase Azure Database tier to get more DTUs and hence accommodate for more IO in your environment. Check Azure SQL Database tiers and pricing options](https://azure.microsoft.com/pricing/details/sql-database/single)
