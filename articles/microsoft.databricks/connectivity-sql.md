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

* Not able to connect to Azure SQL DW using managed identity and ADLS from Databricks getting error similar to: 
    ```
    com.databricks.spark.sqldw.SqlDWSideException: SQL DW failed to execute the JDBC query produced by the connector.
    com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user ‘xxx’. ClientConnectionId: xxx [ErrorCode = 18456] [SQLState = S0001]
    ```
  Issue is most likely due to managed identity misconfiguration on Azure SQL DW. To resolve it, please go through these [steps 1 and 3](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview#steps).


## **Recommended Documents**

* [How To: Connect to Azure Synapse Analytics](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/synapse-analytics)
* [How To: SQL Databases using JDBC](https://docs.microsoft.com/azure/databricks/data/data-sources/sql-databases)
* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Troubleshooting JDBC and ODBC Connections](https://docs.microsoft.com/azure/databricks/kb/bi/jdbc-odbc-troubleshooting)
