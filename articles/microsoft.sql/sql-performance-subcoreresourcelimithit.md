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
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# We ran diagnostics on your resource and found resource limits hit.

<!--issueDescription-->
Our internal service telemetry detected that at <!--$CustomizedEndTime-->CustomizedEndTime<!--/$CustomizedEndTime--> your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** was using a service tier that provides less than one vCore (CPU), **<!--$Slo-->Slo<!--/$Slo-->**, and the database was hitting resource limits in **<!--$Resources-->Resources<!--/$Resources-->**, during <!--$CustomizedStartTime-->CustomizedStartTime<!--/$CustomizedStartTime--> and <!--$CustomizedEndTime-->CustomizedEndTime<!--/$CustomizedEndTime-->.
<!--/issueDescription-->

## **Recommended Steps**

We recommend upgrading the database to a higher service tier **<!--$TargetSlo-->TargetSlo<!--/$TargetSlo-->**, or alternatively, tuning the queries or reducing the overall workload demands.

## **Recommended Documents**

* [Resource limits for single databases using the DTU purchasing model](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases)
* [Resource limits for vCore purchasing model](https://docs.microsoft.com/azure/sql-database/sql-database-vcore-resource-limits-single-databases)
