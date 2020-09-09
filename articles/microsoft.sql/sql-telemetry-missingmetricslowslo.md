<properties
    pageTitle="Database metrics are missing due to low SLO"
    description="Metrics are missing due to low SLO"
    infoBubbleText="Database metrics are missing due to low SLO. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="yujzhan"
    ms.author="yujzhan"
    displayOrder=""
    articleId="MissingMetricsLowSlo_9183A4AE-2FC7-4150-94BF-416B19C15359"
    diagnosticScenario="MissingeMtricsLowSlo"
    selfHelpType="diagnostics"
    supportTopicIds="32630435,32630434,32630412"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="Public, Fairfax, MoonCake, blackforest, usnat, ussec"
    ownershipId="AzureData_AzureSQLDB_Telemetry"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Metrics for database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->** are missing. The database is active, but no metrics are being shown on the Azure Portal.

If basic metrics are missing, this may be due to high resource utilization limits being reached on Basic, S0, S1 and S2 databases. 

If advanced metrics are missing, please note that advanced metrics are only available using the vCore purchasing model with 2 vCores and higher, or 200 DTU and higher for DTU-based purchasing models.
<!--/issueDescription--> 

## **Recommended Steps**

This issue can be mitigated by upgrading the database service tier to S3 or higher.

## **Recommended Documents**
 
* [Scale single database resources in Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/single-database-scale)
* [Resource limits for single databases using the DTU-based purchasing model](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases)