<properties
  pagetitle="Synapse Studio, Azure Portal and Client Tools/SQL Server Management Studio"
  service="microsoft.synapse"
  resource="sqlpools"
  ms.author="saltug,goventur"
  selfhelptype="Generic"
  supporttopicids="32738832"
  resourcetags=""
  productpesids="15818"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="synapse-synapsestudioazureportalandclienttools-sqlservermanagementstudio"
  ownershipid="AzureData_SQLDataWarehouse" />
# Synapse Studio, Azure Portal and Client Tools/SQL Server Management Studio

## **Recommended Steps**

* **Using the Scripting Wizard or connecting with SSMS is slow, not responding or producing errors**

   - Configure SSMS to [generate scripts](https://docs.microsoft.com/sql/ssms/scripting/generate-and-publish-scripts-wizard?view=azure-sqldw-latest#generating-scripts-on-azure-sql-data-warehouse) for Azure SQL Data Warehouse
   - Ensure the user generating the script is created in the master database
   - More information in [Tools Troubleshooting](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-troubleshoot#tools)

* **Generate Script fails in SSMS**

   - Generating a script for Synapse SQL pool fails if the option "Generate script for dependent objects" option is set to "True". As a workaround, click on the menu [Tools]->[Options]->[SQL Server Object Explorer]->[Generate script for dependent options] and set the value to False. More information in [Tools Troubleshooting](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-troubleshoot#tools).
 
* **Install the [latest version of SSMS](https://docs.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms?view=azure-sqldw-latest)**
* **Check for known issues and bug fixes in the [Release Notes](https://docs.microsoft.com/sql/ssms/release-notes-ssms?view=azure-sqldw-latest)**

* **Features currently not supported in SSMS:**

  - SQL Profiler
  - Query Store
  - Backup/Restore
  - Database Diagrams
  - Maintenance plans
  - Import/Export DACPAC

## **Recommended Documents**

* [SQL Server Management Studio (SSMS)](https://docs.microsoft.com/sql/ssms/sql-server-management-studio-ssms?view=azure-sqldw-latest)
* [Connect to SQL pool using SQL Server Management Studio](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-query-ssms)
* [Set up SQL Server Management Studio to script out SQL pool objects](https://docs.microsoft.com/sql/ssms/scripting/generate-and-publish-scripts-wizard?view=azure-sqldw-latest#generating-scripts-on-azure-sql-data-warehouse)
