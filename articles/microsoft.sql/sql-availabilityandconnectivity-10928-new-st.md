<properties
    pageTitle="The session limit for the database has been reached"
    description="Diagnose and resolve issues connecting to Azure SQL Database"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745427"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="CD72434D-E71D-4D81-800B-7AF0A6B97CEC"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# The session limit for the database has been reached

## **Recommended Steps**

### Error 10928: The session limit for the database is X and has been reached

* The Resource ID indicates which resource governance limit is being hit. A value of 1 is a limit on worker threads; 2 is a limit on sessions (connections). For short term mitigation, increase the [service tier](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu?WT.mc_id=pid:13491:sid:32745425/) of your database; longer term, tune the workload so it better fits the selected tier. Refer to the [Query Performance Insight](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance?WT.mc_id=pid:13491:sid:32745425/) feature for assistance analyzing and tuning your workload. <br>
