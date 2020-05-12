<properties
    pageTitle="query execution/high locking waits"
    description="query execution/high locking waits"
    infoBubbleText="Found high locking waits with DB. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="pxding"
    ms.author="pedin"
    displayOrder=""
    articleId="LockWait_E35B0A66-E692-4508-899C-C1C0E5BBB131"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32630434,32630450,32630454,32630459"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# We ran diagnostics on your resource and found high locking waits

<!--issueDescription-->
Our internal service telemetry detected that your Azure SQL DB database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** in server **<!--$ServerName-->ServerName<!--/$ServerName-->** is an instance with high locking waits.
<!--/issueDescription-->

## **Recommended Steps**

This high locking wait event is potentially contributing to performance issues. Please see the recommended article for more details.

## **Recommended Documents**

* [Finding Blocking Queries in SQL Azure](https://azure.microsoft.com/blog/finding-blocking-queries-in-sql-azure)
