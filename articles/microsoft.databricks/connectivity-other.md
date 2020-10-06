<properties
	pageTitle="Diagnose and resolve connectivity issues"
	description="Diagnose and resolve connectivity issues"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677713"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="aad9b1de-3413-4700-97ac-ba5b84675678"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve connectivity issues

To diagnose and resolve connectivity issues, use the following information.

## **Recommended Steps**

* In April 2020, Azure Databricks added **a new unique per-workspace URL for each workspace**. This per-workspace URL has the following format:

    ```
    adb-<workspace-id>.<random-number>.azuredatabricks.net
    ```

This URL is complementary to the existing regional URLs (<region>.azuredatabricks.net) that you have used up until now to access your workspaces. Both URLs continue to be supported. However, because Azure Databricks adds more infrastructure into existing regions, the regional URLs for new workspaces may vary from those of your existing workspaces. We therefore strongly recommend that you **use the new per-workspace URL in scripts or other automation that you want to use with multiple workspaces** by using the instructions in the following links:

   - [How do I launch my workspace using the per-workspace URL?](https://docs.microsoft.com/azure/databricks/workspace/migrate-workspace-urls#how-do-i-launch-my-workspace-using-the-per-workspace-url)

   - [Migrate scripts and other automation](https://docs.microsoft.com/azure/databricks/workspace/migrate-workspace-urls#migrate-scripts-and-other-automation)

    - [Find the regional URL for a workspace](https://docs.microsoft.com/azure/databricks/workspace/migrate-workspace-urls#find-the-regional-url-for-a-workspace)
	
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Use [user-defined routes](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--step-3-create-user-defined-routes-and-associate-them-with-your-azure-databricks-virtual-network-subnets) to solve this problem.

* Use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. You can use the single IP address as an additional security layer with other Azure services and applications that allow access based on specific IP addresses, by following the instructions in [how to assign a single public IP for VNet-injected workspaces using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip).

**Problem:**
  
 You are not able to connect to Azure SQL DW using managed identity and ADLS from Databricks, and you're receiving an error message similar to the following:
  
 ```
 com.databricks.spark.sqldw.SqlDWSideException: SQL DW failed to execute the JDBC query produced by the connector.
 com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user ‘xxx’. ClientConnectionId: xxx [ErrorCode = 18456] [SQLState = S0001]
 ```
  
**Cause:**
  
 The issue is most likely due to managed identity misconfiguration on Azure SQL DW. 
  
**Solution:**
  
 Follow [steps 1 and 3](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview#steps).
  
  **Problem:**
  
  Receiving the following error message when using Databricks cluster with credential passthrough enabled to access SQL datawarehouse via ODBC:
  
  ```
  OperationalError: ('HYT00', '[HYT00] [Microsoft][ODBC Driver 17 for SQL Server]Login timeout expired (0) (SQLDriverConnect)')".
  ```
  
  **Cause:**
  
The pyodbc connection fails because when credential passthrough is enabled on a cluster, the outbound network traffic from Python processes is blocked by design. Also, the SQL database needs some ports to be open, as mentioned in [Ports - ADO.NET](https://docs.microsoft.com/azure/azure-sql/database/adonet-v12-develop-direct-route-ports#inside-client-runs-on-azure).
  
  **Solution:**
  
  Whitelist the required ports by setting Spark configuration in the cluster, making sure to open ports of 1433 and between 11000 and 11999.
  
  ```
  spark.databricks.pyspark.iptable.outbound.whitelisted.ports 1433,11000:11999
  ```

* Implement workload through Azure Firewall to Azure Databricks. Make a note of Azure Databricks control plane endpoints for your workspace (map it based on region of your workspace) when configuring Azure Firewall rules:

|     Name                                                             |     Source                                |     Destination                                                                                                                                                                                                                                 |     Protocol:Port    |     Purpose                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|---------------------------------------------------------------------------------------------------------------|
|     databricks-webapp                                                |     Azure Databricks workspace subnets    |     [Region specific Webapp Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#control-plane-nat-and-webapp-ip-addresses)                                                                |     tcp:443          |     Communication with Azure Databricks webapp                                                                |
|     databricks-log-blob-storage                                      |     Azure Databricks workspace subnets    |     [Region specific Log Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)         |     https:443        |     To store Azure Databricks audit and cluster logs (anonymized / masked) for support and troubleshooting    |
|     databricks-artifact-blob-storage                                 |     Azure Databricks workspace subnets    |     [Region specific Artifact Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)    |     https:443        |     Stores Databricks Runtime images to be deployed on cluster nodes                                          |
|     databricks-dbfs                                                  |     Azure Databricks workspace subnets    |     [DBFS Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#dbfs-root-blob-storage-ip-address)                                                                             |     https:443        |     Azure Databricks workspace root storage                                                                   |
|     databricks-sql-metastore (OPTIONAL – External Hive Metastore)    |     Azure Databricks workspace subnets    |     [Region specific SQL Metastore Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)            |     tcp:3306         |     Stores metadata for databases and child objects in Azure Databricks workspace                             |


## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes

* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)

* [Connect your Azure Databricks Workspace to your On-Premises Network](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network)

* [How to Save Plotly Files and Display From DBFS](https://docs.microsoft.com/azure/databricks/kb/visualizations/save-plotly-to-dbfs)

* [Configure custom DNS](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--option-configure-custom-dns) for VNet- injected workspaces
