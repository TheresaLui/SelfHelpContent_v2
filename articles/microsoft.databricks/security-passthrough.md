<properties
	pageTitle="Diagnose and resolve issues with Pass Through Security"
	description="Diagnose and resolve issues with Pass Through Security"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677721"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="f1dae65e-2eee-4c5e-bbd3-4a1310313f3d"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Pass Through Security

## **Recommended Steps**

* **Problem**
  
  Getting the following error when using Databricks cluster with credential passthrough enabled to access SQL datawarehouse via ODBC:
  
  ```
  OperationalError: ('HYT00', '[HYT00] [Microsoft][ODBC Driver 17 for SQL Server]Login timeout expired (0) (SQLDriverConnect)')".
  ```
  
  **Cause**
  
  The pyodbc connection fails because when credential passthrough is enabled on a cluster, outbound network traffic from python processes is blocked by design. And SQL database needs some ports to be open as mentioned in [Ports - ADO.NET](https://docs.microsoft.com/azure/azure-sql/database/adonet-v12-develop-direct-route-ports#inside-client-runs-on-azure).
  
  **Solution**
  
  Whitelist the required ports by setting Spark configuration in cluster making sure to open ports of 1433 and between 11000 and 11999.
  
  ```
  spark.databricks.pyspark.iptable.outbound.whitelisted.ports 1433,11000:11999
  ```
 
 
* **Problem**

  Getting this exception on High Concurrency cluster with Credential Passthrough enabled: 

  ```
  py4j.security.Py4JSecurityException: … is not whitelisted
  ```
  **Cause**

  This exception is thrown when you have accessed a method that Azure Databricks has not explicitly marked as safe for Azure Data Lake Storage credential passthrough clusters. In most cases, this means that the method could allow a user on a Azure Data Lake Storage credential passthrough cluster to access another user’s credentials.

  **Solution**

  1) You can either disable Credential Passthrough for this HC cluster
  2) Or use Standard cluster with Credential Passthrough enabled where single user access is allowed


## **Recommended Documents**

* [Security and Privacy](https://docs.microsoft.com/azure/databricks/security/)
* [AAD Credential Passthrough](https://docs.microsoft.com/azure/databricks/security/credential-passthrough/adls-passthrough)
* [Retrieve the current username for the notebook](https://docs.microsoft.com/azure/databricks/kb/notebooks/get-notebook-username). This is currently supported for:
	* Standard clusters in both Scala and Python
	* High Concurrency clusters in Python with Credential Passthrough **disabled**
