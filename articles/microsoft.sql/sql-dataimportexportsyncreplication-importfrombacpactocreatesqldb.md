<properties
	pageTitle="data import, export, sync, replication/import from BACPAC to create SQL db"
	description="data import, export, sync, replication/import from BACPAC to create SQL db"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630430"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="f291a9f3-4717-4279-a7fa-aa081acffc13"
	ownershipId="AzureData_AzureSQLDB_ImportExport"
/>

# BACPAC, DataSync, Copy DB and Replication/import from BACPAC to create SQL db

SQL DB Import service supports importing a BACPAC file into a new Azure SQL database. For databases over 150 GBs, we recommend using [sqlpackage.exe](https://docs.microsoft.com/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility) to perform the import.

## **Recommended Steps**

### BlobUri could not be found for this request

* While retrieving the status of a request there are edge cases where the service will return a status of "Completed" and an error message of "BlobUri could not be found for this request". In these cases, the Import operation has completed successfully and the error message can be safely ignored.

### Unable to authenticate request/Login failed for user

* Import service does not support multi-factor authentication (MFA). If you are using AAD, make sure MFA is disabled and retry the import. If MFA is required, please use [sqlpackage.exe](https://docs.microsoft.com/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility).

### There is an import or export operation in progress on the database

* Import service does not allow issuing multiple requests for the same database. Please wait until the current operation is finished.

### Failure with code 504

* This is most commonly caused when the server's firewall is blocking the Export service. Make sure to [add a rule to the server's firewall to allow access from Azure services](https://docs.microsoft.com/azure/sql-database/sql-database-firewall-configure#manage-server-level-ip-firewall-rules-using-the-azure-portal).

### Import operation has been running for a long time (or progress seems stuck)

* Import speed depends on the following factors:

	* The data shape (schema) and the data size
	* The volume of export requests submitted simultaneously in a region. In situations where the volume of requests is very high, an import job can spend considerable time [waiting for resources to become available before it can start](https://support.microsoft.com/help/2965554/azure-sql-database-import-export-service-takes-a-long-time-to-import-o).

* To get the best performance, we recommend:

  * Using [sqlpackage.exe](https://docs.microsoft.com/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility)
  * Importing to a higher SLO and downgrading after the import has finished. This has a big impact on performance, particularly for lower service tiers.
  * Making sure the storage account containing the BACPAC file is in the same region as the database to avoid any unnecessary network latencies

### Cancelling the import job

* This capability is not yet available to customers. We are actively working on it. In the meantime, please file a ticket to get your import cancelled.

## **Recommended Documents**

* More details can be found in [Import a BACPAC file to a new Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-export?WT.mc_id=pid:13491:sid:32630420/)
