<properties
    pageTitle="There is no login activity to the database."
    description="No login activity"
    infoBubbleText="There is no login activity to the database. See details on the right."
    service="microsoft.sql"
    resource="servers"
    resourceTags="databases"
    authors="yujzhan"
    ms.author="yujzhan"
    displayOrder=""
    articleId="MissingMetricsNoLogin_5319F4E2-A2DA-426D-B9D9-E6F321380252"
    diagnosticScenario="MissingMetricsNoLogin"
    selfHelpType="diagnostics"
    supportTopicIds="32630435,32630434"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="Public, Fairfax, MoonCake, usnat, ussec"
    ownershipId="AzureData_AzureSQLDB_Telemetry"
/>

# Database metrics are missing due to no connections to the database

<!--issueDescription-->
Between **<!--$StartTime-->StartTime<!--/$StartTime-->** UTC and **<!--$EndTime-->EndTime<!--/$EndTime-->** UTC, there were no connections to the database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->**. So there will not be any cpu metrics uploaded. This means that the customer will not see cpu/dtu metrics for this database on the Azure Portal.
<!--/issueDescription-->

## **Recommended Steps**

Inform the customer that there were no logins to the given database. As a result, there will be no CPU/DTU metrics by design.