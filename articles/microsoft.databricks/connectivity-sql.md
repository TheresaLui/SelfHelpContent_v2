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

* **Problem**

 The Cosmos DB account firewall is blocking Databricks requests, resulting in the following error:

  ```
  Uncaught throwable from user code: com.microsoft.azure.documentdb.DocumentClientException: Request originated from client IP xx.xx.xxx.xxx through public internet. This is blocked by your Cosmos DB account firewall settings.
  ```
  
  **Solution**
  
  * **VNet injected workspace** - Doublec-heck your Cosmos DB account firewall settings and add the service endpoint for Databricks VNet and subnet.
  * **Non VNet injected workspace** - Azure IP ranges are periodically refreshed in the configuration, so make sure to add tje Databricks service IP range to your Cosmos DB account firewall settings. 
  
     * Check the [new IP ranges with Azure IP ranges and Service Tags](https://www.microsoft.com/download/details.aspx?id=56519). This file contains the IP address ranges for Public Azure as a whole, each Azure region within Public, and ranges for several Azure Services (Service Tags) in Public. This file is updated weekly. New ranges appearing in the file will not be used in Azure for at least one week. Download the new JSON file every week and perform the necessary changes at your site to correctly identify services running in Azure. 
     
     * The Cosmos DB team is working on improvements for this issue that will eliminate the lag in updating the IP ranges in Cosmos configuration used to evaluate Azure IP ranges. These improvements require substantial changes and will be in production in February 2021.  
     
     * A **recommended** workaround: Create a new VNet injected workspace and add the service endpoint for its VNet and subnet in Cosmos DB account firewall settings.
      
  
* **Problem**

  Not able to connect to Azure SQL DW using managed identity and ADLS from Databricks, and receiving an error similar to the following: 
  
  ```
  com.databricks.spark.sqldw.SqlDWSideException: SQL DW failed to execute the JDBC query produced by the connector.
  com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user ‘xxx’. ClientConnectionId: xxx [ErrorCode = 18456] [SQLState = S0001]
  ```
  **Cause**
  
  This is most likely due to managed identity misconfiguration on Azure SQL DW. 
  
  **Solution**
  
  Follow [steps 1 and 3 on this page](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview#steps).

* **Problem**
  
  Using Databricks cluster with credential passthrough enabled to access SQL datawarehouse through ODBC, and receiving the following error:
  
  ```
  OperationalError: ('HYT00', '[HYT00] [Microsoft][ODBC Driver 17 for SQL Server]Login timeout expired (0) (SQLDriverConnect)')".
  ```
  
  **Cause**
  
  The pyodbc connection fails because when credential passthrough is enabled on a cluster, outbound network traffic from Python processes is blocked by design. Additionally, SQL database needs some ports to be open, as mentioned in [Ports - ADO.NET](https://docs.microsoft.com/azure/azure-sql/database/adonet-v12-develop-direct-route-ports#inside-client-runs-on-azure).
  
  **Solution**
  
  Whitelist the required ports by setting a Spark configuration in the cluster. Make sure to open port 1433 and ports between 11000 and 11999:
  
  ```
  spark.databricks.pyspark.iptable.outbound.whitelisted.ports 1433,11000:11999
  ```

* **Problem**
  
  Azure Databricks commands connecting to Azure Data Warehouse through Spark Synapse Connector fail, with the following error:

  ```
  com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user 'XXX'. ClientConnectionId:XXXX [ErrorCode = 18456] [SQLState = S0001]
  ```

  **Cause** 
  
  This is possibly due to Azure DW server not accepting the password when sent through the URL because it contains characters that are changed after URL encoding.

  **Solution** 

  Use the connector option to add the password instead of through the URL, or use a password that is encoded safe for the URL.
  
## **Recommended Documents**

* [How To: Connect to Azure Synapse Analytics](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/synapse-analytics)
* [How To: SQL Databases using JDBC](https://docs.microsoft.com/azure/databricks/data/data-sources/sql-databases)
* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Troubleshooting JDBC and ODBC Connections](https://docs.microsoft.com/azure/databricks/kb/bi/jdbc-odbc-troubleshooting)
