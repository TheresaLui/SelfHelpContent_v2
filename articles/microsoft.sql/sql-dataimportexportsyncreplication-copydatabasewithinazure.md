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

# Database Copy

*Database copy* is a transactionally consistent snapshot of your source database as a point-in-time after the copy is initiated.  The copy is created using the geo-replication technology.  All the requirements for  [using geo-replication](https://docs.microsoft.com/azure/azure-sql/database/active-geo-replication-overview) apply to the database copy operation. Once replica seeding is complete, the geo-replication link is automatically terminated.

### **Login and other failures on copied Database**

* After the copy operation to a different server succeeds, and before other users are remapped, only the login associated with the database owner, or the server administrator can log in to the copied database. To resolve logins and establish data access after the copying operation is complete, see [Resolve logins](https://docs.microsoft.com/azure/azure-sql/database/database-copy?tabs=azure-powershell#resolve-logins)

* *Error : Database '(Copied database name)' on server '(Target Server)' is not currently available.  Please retry the connection later.*
This means, the copy (seeding) operation is still in progress and in this case you need to wait until the DB copy operation is complete. Depending on the size of the database & target service tier the process the duration varies. However if the problem persists for longer duration, please proceed with creating support request and provide the tracing ID.

* If you receive permission related errors when you create or cancel a database copy request, please ensure you have *Subscription Owner* Or *SQL Server Contributor role*  or *Custom role on the source and target databases with following permission:  Microsoft.Sql/servers/databases/read Microsoft.Sql/servers/databases/write*

## **Recommended documents**

* [DB   Copy using  Azure portal](https://docs.microsoft.com/azure/sql-database/sql-database-copy?tabs=azure-powershell#copy-a-database-by-using-the-azure-portal)
* [DB Copy Using PowerShell or Azure CLI](https://docs.microsoft.com/azure/azure-sql/database/database-copy?tabs=azure-powershell#copy-using-powershell-or-the-azure-cli)
* [DB Copy Using Transact-SQL](https://docs.microsoft.com/azure/azure-sql/database/database-copy?tabs=azure-powershell#copy-using-transact-sql)
* [Copy DB to a different subscription](https://docs.microsoft.com/azure/sql-database/sql-database-copy?tabs=azure-powershell#copy-a-sql-database-to-a-different-subscription) <br>
