<properties
	pageTitle="data import, export, sync, replication/export from SQL db to BACPAC"
	description="data import, export, sync, replication/export from SQL db to BACPAC"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630420"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="12410211-a2f0-48af-99a1-58da8fcb50ff"
	ownershipId="AzureData_AzureSQLDB_ImportExport"
/>

# BACPAC, DataSync, Copy DB and Replication/export from SQL db to BACPAC

SQL DB Export service supports exporting an Azure SQL database to a BACPAC file. For databases over 150 GBs, we recommend using [`sqlpackage.exe`](https://docs.microsoft.com/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility) to perform the export.

## **Recommended Steps**

### BlobUri could not be found for this request

* While retrieving the status of a request there are edge cases where the service will return a status of **Completed** and the error message, "BlobUri could not be found for this request". In these cases, the Export operation has completed successfully and the error message can be safely ignored.

### Unable to authenticate request

* Export service does not support multi-factor authentication (MFA). If you're using AAD, make sure MFA is disabled and retry the export. If MFA is required, please use [sqlpackage.exe](https://docs.microsoft.com/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility).

### There is an import or export operation in progress on the database

* Export service does not allow multiple requests for the same database. Wait until the current operation is finished to issue a new request.

### Cancel the export job

* Use the REST API or PowerShell to cancel asynchronous update operations on the database.
	* [Database Operations - Cancel using REST API](https://docs.microsoft.com/rest/api/sql/databaseoperations/cancel)
	* [Database Operations - Cancel using PowerShell](https://docs.microsoft.com/powershell/module/az.sql/Stop-AzSqlDatabaseActivity?view=azps-5.5.0&viewFallbackFrom=azps-5.0.0)
	* If there are any issues cancelling the operation, or if you're unable to cancel using above options, file a ticket to get your export cancelled.

### Blob already exists

* A BACPAC file with the same name already exists in Azure Blob storage. Choose a different name for the file.

### Failure with code 504

* This is most commonly caused when the server's firewall blocks the Export service. Make sure to [add a rule to the server's firewall to allow access from Azure services](https://docs.microsoft.com/azure/sql-database/sql-database-firewall-configure#manage-server-level-ip-firewall-rules-using-the-azure-portal).

### Export operation has been running for a long time (or progress seems stuck)

* Export speed depends on the following factors:

	* The data shape (schema) and the data size
	* The volume of export requests submitted simultaneously in a region. In situations where the volume of requests is very high, an export job can spend considerable time [waiting for resources to become available before it can start](https://support.microsoft.com/help/2965554/azure-sql-database-import-export-service-takes-a-long-time-to-import-o).

 * To get the best performance, we recommend the following:
 
    * Use [`sqlpackage.exe`](https://docs.microsoft.com/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility)
    * Make sure no other workload is running on the database. Creating a copy before export may be the best solution to ensure no other workload.
    * Increase database SLO to better handle the export workload (primarily read IO)
    * Make sure there are clustered indexes particularly for large tables
    * Make sure that the storage account where the BACPAC file will be saved is in the same region as the database to avoid unnecessary network latencies

## **Recommended Documents**

* For an export to be transactionally consistent, you must ensure that no write activity occurs during the export, or that you're exporting from a [transactionally consistent](https://docs.microsoft.com/azure/sql-database/sql-database-copy) copy of your Azure SQL database
* More details can be found in [Export an Azure SQL database to a BACPAC file](https://docs.microsoft.com/azure/sql-database/sql-database-export?WT.mc_id=pid:13491:sid:32630420/)
