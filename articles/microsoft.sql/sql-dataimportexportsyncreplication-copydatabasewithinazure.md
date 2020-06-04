<properties
    pageTitle="data import, export, sync, replication/copy database within Azure"
    description="data import, export, sync, replication/copy database within Azure"
    service="microsoft.sql"
    resource="servers"
    authors="emlisa"
    ms.author="emlisa"
    displayOrder="7"
    selfHelpType="generic"
    supportTopicIds="32630415"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="514fdf6b-b8b0-4887-a734-2236d1907bff"
    ownershipId="AzureData_AzureSQLDB_GeoDr"
/>

# data import, export, sync, replication/copy database within Azure

## **Recommended Steps**

The following details explain how to migrate or move database. <br>

* Copy a database within the same subscription can be done:
    * [Using the Azure portal](https://docs.microsoft.com/azure/sql-database/sql-database-copy?tabs=azure-powershell#copy-a-database-by-using-the-azure-portal)<br>
    * [Using PowerShell or Azure CLI](https://docs.microsoft.com/azure/sql-database/sql-database-copy#copy-a-database-by-using-powershell-or-azure-cli)<br>
    * [Using Transact-SQL](https://docs.microsoft.com/azure/sql-database/sql-database-copy#copy-a-database-by-using-transact-sql)<br>
* To copy a SQL database to a [different subscription](https://docs.microsoft.com/azure/sql-database/sql-database-copy?tabs=azure-powershell#copy-a-sql-database-to-a-different-subscription) you can Transact-SQL.<br>
* To move the logical server and all it's databases to a new resource group or subscription within the same region, click "Move" at the top of the SQL server resource blade that hosts your database. Note: Databases cannot be moved individually.<br>
* To move Azure SQL resources to another region please check [this article](https://docs.microsoft.com/azure/sql-database/sql-database-move-resources-across-regions).
* To [migrate an SQL Server database to Azure SQL](https://azure.microsoft.com/documentation/articles/sql-database-cloud-migrate?WT.mc_id=pid:13491:sid:32630415/), first run the compatibility tool to determine whether it can be migrated, fix any incompatibility issues, then select an appropriate migration method.<br>
* Create a copy of a database so it can be used outside of Azure: [Export a BACPAC file](https://azure.microsoft.com/documentation/articles/sql-database-export?WT.mc_id=pid:13491:sid:32630415/)<br>

## **Recommended Documents**

* [Copy a transactionally consistent copy of an Azure SQL database](https://docs.microsoft.com/azure/sql-database/sql-database-copy?tabs=azure-powershell)<br>
* [Move resources to a new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription)<br>
