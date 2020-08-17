<properties
    pageTitle="Database metrics are missing due to low SLO"
    description="Metrics are missing due to low SLO"
    infoBubbleText="Database metrics are missing due to low SLO. See details on the right."
    service="microsoft.sql"
    resource="servers"
    resourceTags="databases"
    authors="yujzhan"
    ms.author="yujzhan"
    displayOrder=""
    articleId="MissingMetricsLowSlo_9183A4AE-2FC7-4150-94BF-416B19C15359"
    diagnosticScenario="MissingMetricsLowSlo"
    selfHelpType="diagnostics"
    supportTopicIds="32630435,32630434"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="Public, Fairfax, MoonCake, usnat, ussec"
    ownershipId="AzureData_AzureSQLDB_Telemetry"
/>

# Database metrics are missing due to low SLO

<!--issueDescription-->
Between **<!--$StartTime-->StartTime<!--/$StartTime-->** UTC and **<!--$EndTime-->EndTime<!--/$EndTime-->** UTC, metrics for database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->** appear to be missing. The database is active, but no metrics are being uploaded. This means that the customer will not see metrics for this database on the Azure Portal.Database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->** has a low SLO of **<!--$ServiceLevelObjective-->ServiceLevelObjective<!--/$ServiceLevelObjective-->**. For databases with low SLOs (Free, Basic, S0, S1, and S2), missing metric issues are typically caused by a lack of available memory for Monitoring Agent - the application that uploads database metrics.
<!--/issueDescription-->

## **Recommended Steps**

This issue can be mitigated by upgrading the database SLO to S3 or higher. Databases on lower SLOs (Free, Basic, S0, S1, and S2) may continue to see this issue due to by-design CPU and memory limitations.