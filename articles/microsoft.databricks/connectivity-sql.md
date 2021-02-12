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

Use this document to resolve many common connectivity issues related to SQL resources.  

* **Problem**: The Cosmos DB account firewall is blocking Databricks requests, resulting in the error:<br>
   "Uncaught throwable from user code: com.microsoft.azure.documentdb.DocumentClientException: Request originated from client IP xx.xx.xxx.xxx through public internet. This is blocked by your Cosmos DB account firewall settings." 
  
  **Solution**
  
  * **VNet injected workspace** - Double-check your Cosmos DB account firewall settings, and add the service endpoint for Databricks VNet and subnet.
  * **Non VNet injected workspace** - Azure IP ranges are periodically refreshed in the configuration. Make sure to add the Databricks service IP range to your Cosmos DB account firewall settings. 
  
     * Check the [new IP ranges with Azure IP ranges and Service Tags](https://www.microsoft.com/download/details.aspx?id=56519). This file contains the IP address ranges for: Public Azure as a whole, each Azure region within Public, and ranges for several Azure Services (Service Tags) in Public. This file is updated weekly. New ranges that appear in the file will not be used in Azure for at least one week. Download the new JSON file each week and perform the necessary changes at your site to correctly identify services running in Azure. 
     
     * A **recommended** workaround: Create a new VNet injected workspace. Add the service endpoint for its VNet and subnet in the Cosmos DB account firewall settings.
      
     * The Cosmos DB team is working to eliminate the lag in updating the IP ranges in Cosmos configuration which are used to evaluate Azure IP ranges. These improvements require substantial changes and will be in production in February 2021.
  
* **Problem**: Unable to connect to Azure SQL DW using managed identity and ADLS from Databricks, resulting in an error similar to the following: <br>
  "com.databricks.spark.sqldw.SqlDWSideException: SQL DW failed to execute the JDBC query produced by the connector.
  com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user ‘xxx’. ClientConnectionId: xxx [ErrorCode = 18456] [SQLState = S0001]" 

  **Cause**: This is likely due to managed identity misconfiguration on Azure SQL DW.
  
  **Solution**: Follow [steps 1 and 3 on this Help page](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview#steps).
  

* **Problem**: Using Databricks cluster with credential passthrough enabled to access SQL datawarehouse through ODBC, results in the following error: <br>
  "OperationalError: ('HYT00', '[HYT00] [Microsoft][ODBC Driver 17 for SQL Server]Login timeout expired (0) (SQLDriverConnect)')"."
  
  **Cause**: The pyodbc connection fails because when credential passthrough is enabled on a cluster, outbound network traffic from Python processes is blocked by design. Additionally, SQL database needs some ports to be open, as mentioned in [Ports - ADO.NET](https://docs.microsoft.com/azure/azure-sql/database/adonet-v12-develop-direct-route-ports#inside-client-runs-on-azure).
  
  **Solution**: Set a Spark configuration in the cluster to add the required ports to the allow list. Make sure to open port 1433 and ports between 11000 and 11999:
  
  ```
  spark.databricks.pyspark.iptable.outbound.whitelisted.ports 1433,11000:11999
  ```

* **Problem**: Azure Databricks commands connecting to Azure Data Warehouse through Spark Synapse Connector fail, with the following error:<br>
  "com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user 'XXX'. ClientConnectionId:XXXX [ErrorCode = 18456] [SQLState = S0001]"

  **Cause**: This issue may be caused by the Azure DW server not accepting the password when sent through the URL because it contains characters that are changed after URL encoding.

  **Solution**: Use the connector option to add the password, or use a password that is encoded safe for the URL.
  
 
* **Problem**: Pulling data from Azure Synapse exceeds the Polybase max row size limitation, resulting in the error:
  "com.microsoft.sqlserver.jdbc.SQLServerException: Polybase export failed. The size of a row is xxxxx bytes. It exceeds the maximum allowed row size of 1000000 bytes for Polybase. Consider reducing the number of columns. [ErrorCode = 105062] [SQLState = S0001]"

  **Cause**: According to the [Azure Synapse documentation](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-service-capacity-limits#loads), the limitation for Polybase loads is 1 MB per row. 

  **Solution**: Consider reducing the number of columns.
  
* **Problem**: Experiencing issues when attempting to connect from Azure Databricks to Azure SQL Server via PyODBC/ODBC driver getting error **[Login timeout expired (0)]** or via SSMS getting **Error 10060** clearly stating a connection attempt failed because the connected party did not respond after a period of time.

  **Cause**: If you have correctly followed [this document](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/synapse-analytics) to establish a proper connection, issue would be caused by NSG is not being correctly configured and thus connection to the database could not be established.

  **Solution**: After these ports are allow listed, you should be able to connect successfully to the target database using SQL Credentials. 
    * Make sure NSG have **ports 80, 443, and 1433** allowed through the firewall.
    * As per the [Azure Connectivity architecture](https://docs.microsoft.com/azure/azure-sql/database/connectivity-architecture) when the connection is within the Azure boundary we make use of redirection which requires **port Range 11000 to 11999** to be opened as well, when the host is outside of the Azure network it would be a Proxy connection making use of Port 1433 only.
  
      The Firewall rules on the Logical Server allow you to change the [connection policy](https://docs.microsoft.com/azure/azure-sql/database/connectivity-architecture#connection-policy) for all inbound connections to Proxy, when doing so only Port 1433 will be required. 

  
  
## **Recommended Documents**

* [How To: Connect to Azure Synapse Analytics](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/synapse-analytics)
* [How To: SQL Databases using JDBC](https://docs.microsoft.com/azure/databricks/data/data-sources/sql-databases)
* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Troubleshooting JDBC and ODBC Connections](https://docs.microsoft.com/azure/databricks/kb/bi/jdbc-odbc-troubleshooting)
