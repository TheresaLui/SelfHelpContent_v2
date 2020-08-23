<properties
    pageTitle="data import, export, sync, replication/copy database within Azure"
    description="data import, export, sync, replication/copy database within Azure"
    service="microsoft.sql"
    resource="servers"
    authors="subbuk"
    ms.author="subbuk"
    displayOrder="7"
    selfHelpType="generic"
    supportTopicIds="32630415"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="514fdf6b-b8b0-4887-a734-2236d1907bff"
    ownershipId="AzureData_AzureSQLDB_GeoDr"
/>

# Database copy

**DB Copy Operation**

Database Copy is a transactionally consistent snapshot of your source database as a point-in-time after the copy is initiated.  The copy is created using the geo-replication technology.  All the requirements for  [using geo-replication](https://docs.microsoft.com/azure/azure-sql/database/active-geo-replication-overview) apply to the database copy operation. Once replica seeding is complete, the geo-replication link is automatically terminated


## **Recommended Documents**
[DB   Copy using  Azure portal](https://docs.microsoft.com/azure/sql-database/sql-database-copy?tabs=azure-powershell#copy-a-database-by-using-the-azure-portal)
