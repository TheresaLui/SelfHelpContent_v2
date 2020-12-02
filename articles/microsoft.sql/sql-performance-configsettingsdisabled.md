<properties
    pageTitle="performance/configuration settings disabled"
    description="performance/configuration settings disabled"
    infoBubbleText="Found configuration settings disabled on this database. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="ketho00"
    ms.author="ketho"
    displayOrder=""
    articleId="ConfigSettingsDisabled_4f775a06-7699-4fed-b558-f11faf80a73e"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32749512,32749514,32749515,32749518,32749520"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="Public,Mooncake,fairfax,usnat,ussec"
    ownershipId="AzureData_AzureSQLDB_Performance"
/>

# We ran diagnostics on your resource and found configuration settings disabled.

<!--issueDescription-->
Our internal service telemetry detected that certain configuration settings are disabled on the database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on the server **<!--$ServerName-->ServerName<!--/$ServerName-->** between **<!--$StartTime-->StartTime<!--/$StartTime--> UTC** and **<!--$EndTime-->EndTime<!--/$EndTime--> UTC**. <!--$message-->message<!--/$message-->
<!--/issueDescription-->

## **Recommended Steps**

<!--$recommendation-->recommendation<!--/$recommendation-->

## **Recommended Documents**

* [Automatic Tuning](https://docs.microsoft.com/sql/relational-databases/automatic-tuning/automatic-tuning?view=sql-server-2017)
* [SQL Server Statistics Overview](https://docs.microsoft.com/sql/relational-databases/statistics/statistics?view=sql-server-2017)
* [Turn on Auto Update Statistics](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-set-options?view=sql-server-2017#auto_update_statistics)
* [Turn on Auto Create Statistics](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-set-options?view=sql-server-2017#auto_update_statistics)
* [Tune Azure SQL MaxDOP setting with Alter Database](https://docs.microsoft.com/sql/t-sql/statements/alter-database-scoped-configuration-transact-sql?view=sql-server-2017)
* [Monitoring Performance by using the Query Store](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?view=sql-server-ver15)
