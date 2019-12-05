<properties
    pageTitle="performance/subcore tiers resource limits hit"
    description="performance/subcore tiers resource limits hit"
    infoBubbleText="Found resource limits hit on this subcore DB. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="changslMS"
    ms.author="changsl"
    displayOrder=""
    articleId="Subcore_166C42B9-A932-407E-A9AE-4B454D7986BF"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32630434,32630450,32630459"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake"
/>

# We ran diagnostics on your resource and found resource limits hit.

<!--issueDescription-->
Our internal service telemetry detected that your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** is currently using the sub-core service tier **<!--$Slo-->Slo<!--/$Slo-->** and hitting the resource limit in **<!--$Category-->Category<!--/$Category-->**.
<!--/issueDescription-->

## **Recommended Steps**

Recommend upgrading the database to a higher service tier **<!--$TargetSlo-->TargetSlo<!--/$TargetSlo-->**, or tuning the queries/reducing the workload demands.

## **Recommended Documents**

* [Resource Limits for Sub-core Tiers](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases)
* [Resource Limits for vCore Purchasing Model](https://docs.microsoft.com/azure/sql-database/sql-database-vcore-resource-limits-single-databases)
