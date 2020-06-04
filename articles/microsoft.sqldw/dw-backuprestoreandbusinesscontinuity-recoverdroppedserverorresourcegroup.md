<properties
    pageTitle="Recover dropped server or resource group"
    description="Recover dropped server or resource group"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635215"
    productPesIds="15818"
    displayOrder="72"
    selfHelpType="generic"
    resourceTags="datawarehouse"
    articleId="dw-backuprestoreandbusinesscontinuity-recoverdroppedserverorresourcegroup.md"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Recovering a dropped server

If you delete an Azure SQL Warehouse server, all data warehouses are also deleted and cannot be recovered.

File a support ticket to attempt recovery of the dropped server. Best chances of recovery are if:

* A server with the same name has not been created
* The server was dropped less than 7 days ago

To learn how to avoid business interruptions you can review the capabilities that Azure SQL Database provides for [business continuity](https://docs.microsoft.com/azure/sql-data-warehouse/backup-and-restore).

## **Recommended Steps**

Check if the databases under the server can be recovered using supported features:

* If the server still exists you can [restore deleted databases](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-restore-deleted-dw) from the Azure portal, PowerShell, or REST APIs
