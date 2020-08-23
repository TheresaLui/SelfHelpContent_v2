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

*Database copy* is a transactionally consistent snapshot of your source database as a point-in-time after the copy is initiated.  The copy is created using the geo-replication technology.  All the requirements for  [using geo-replication](https://docs.microsoft.com/azure/azure-sql/database/active-geo-replication-overview) apply to the database copy operation. Once replica seeding is complete, the geo-replication link is automatically terminated.

**Logins for Copied DB**
- The logins, users, and permissions in the copied database are managed independently from the source database.
- When you copy a database to a different server, the security principal that initiated the copy operation on the target server becomes the owner of the new database.
- Regardless of the target server, all database users, their permissions, and their security identifiers (SIDs) are copied to the database copy.
- Using contained database users for data access ensures that the copied database has the same user credentials, so that after the copy is complete you can immediately access it with the same credentials.

## **Recommended Documents**
[DB   Copy using  Azure portal](https://docs.microsoft.com/azure/sql-database/sql-database-copy?tabs=azure-powershell#copy-a-database-by-using-the-azure-portal)
