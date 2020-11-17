<properties
	pageTitle="Diagnose and resolve connectivity issues to SQL Resources"
	description="Diagnose and resolve connectivity issues to SQL Resources"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677675"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="02b9be12-7855-42a0-b3b9-89342f2360fd"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve connectivity issues to SQL Resources

## **Recommended Steps**

* **Problem:**

  Not able to connect to Azure SQL DW using managed identity and ADLS from Databricks getting error similar to: 
  
  ```
  com.databricks.spark.sqldw.SqlDWSideException: SQL DW failed to execute the JDBC query produced by the connector.
  com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user ‘xxx’. ClientConnectionId: xxx [ErrorCode = 18456] [SQLState = S0001]
  ```
  **Cause:**
  
  Issue is most likely due to managed identity misconfiguration on Azure SQL DW. 
  
  **Solution:**
  
  Please go through these [steps 1 and 3](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview#steps).

* **Problem:**
  
  Getting the following error when using Databricks cluster with credential passthrough enabled to access SQL datawarehouse via ODBC:
  
  ```
  OperationalError: ('HYT00', '[HYT00] [Microsoft][ODBC Driver 17 for SQL Server]Login timeout expired (0) (SQLDriverConnect)')".
  ```
  
  **Cause:**
  
  The pyodbc connection fails because when credential passthrough is enabled on a cluster, outbound network traffic from python processes is blocked by design. And SQL database needs some ports to be open as mentioned in [Ports - ADO.NET](https://docs.microsoft.com/azure/azure-sql/database/adonet-v12-develop-direct-route-ports#inside-client-runs-on-azure).
  
  **Solution:**
  
  Whitelist the required ports by setting Spark configuration in cluster making sure to open ports of 1433 and between 11000 and 11999.
  
  ```
  spark.databricks.pyspark.iptable.outbound.whitelisted.ports 1433,11000:11999
  ```

* **Problem:**
  
  Azure Databricks commands connecting to Azure Data Warehouse via Spark Synapse Connector fail with error:

  ```
  com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user 'XXX'. ClientConnectionId:XXXX [ErrorCode = 18456] [SQLState = S0001]
  ```

  **Cause:** 
  
  This is possibly due to Azure DW server does not accept the password when sent via URL because it contains characters that are changed after URL encoding.

  **Solution:** 

  Use the connector option to add the password instead of via the URL or use a password that is URL encode safe.
  
## **Recommended Documents**

* [How To: Connect to Azure Synapse Analytics](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/synapse-analytics)
* [How To: SQL Databases using JDBC](https://docs.microsoft.com/azure/databricks/data/data-sources/sql-databases)
* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Troubleshooting JDBC and ODBC Connections](https://docs.microsoft.com/azure/databricks/kb/bi/jdbc-odbc-troubleshooting)
