<properties
    pageTitle="There is no login activity to the database."
    description="No login activity"
    infoBubbleText="There is no login activity to the database. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="yujzhan"
    ms.author="yujzhan"
    displayOrder=""
    articleId="MissingMetricsNoLogin_5319F4E2-A2DA-426D-B9D9-E6F321380252"
    diagnosticScenario="SqlMetrics"
    selfHelpType="diagnostics"
    supportTopicIds="32630435,32630434,32630412"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="Public, Fairfax, MoonCake, blackforest, usnat, ussec"
    ownershipId="AzureData_AzureSQLDB_Telemetry"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Due to inactivity in database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->** , the metric value is zero. The metric is still being emitted and has the correct value.
<!--/issueDescription-->

## **Recommended Steps**

To resume the flow of database metrics, connect to the database and run a query.

## **Recommended Documents**
 
* [Monitoring and performance tuning in Azure SQL Database and Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/database/monitor-tune-overview)