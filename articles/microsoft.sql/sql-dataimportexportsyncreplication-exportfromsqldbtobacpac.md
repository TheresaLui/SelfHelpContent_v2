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
	cloudEnvironments="public"
	articleId="12410211-a2f0-48af-99a1-58da8fcb50ff"
/>

# data import, export, sync, replication/export from SQL db to BACPAC

SQL DB Export service supports exporting an Azure SQL database to a BACPAC file. For large databases (over 250 GBs), we recommend using [sqlpackage.exe](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility) to perform the export.

### **Recommended Solutions**

### Unable to authenticate request

* Export service does not support multi-factor authentication (MFA). If you are using AAD, make sure MFA is disabled and retry the export. If MFA is required, please use [sqlpackage.exe](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility).<br>

### There is an import or export operation in progress on the database

* Export service does not allow issuing multiple requests for the same database. Please wait until the current operation is finished.

### Blob already exists

* A bacpac file with the same name already exists in Azure Blob storage. Please choose a different name for the file.

### Failure with code 504

* This is most commonnly caused when the server's firewall is blocking the Export service. Make sure to [add a rule to the server's firewall to allow access from Azure services](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-firewall-configure#manage-server-level-ip-firewall-rules-using-the-azure-portal).

## **Recommended Documents**

* For an export to be transactionally consistent, you must ensure either that no write activity is occurring during the export, or that you are exporting from a [transactionally consistent](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-copy) copy of your Azure SQL database.

* More details can be found in [Export an Azure SQL database to a BACPAC file](https://docs.microsoft.com/azure/sql-database/sql-database-export?WT.mc_id=pid:13491:sid:32630420/)
