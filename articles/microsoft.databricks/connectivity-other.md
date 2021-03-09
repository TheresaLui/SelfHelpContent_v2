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

> **Check [Azure Databricks status page](https://status.azuredatabricks.net/) for current status by region. We highly recommend subscribing for updates on this page, which will automatically notify you of future status changes.**

 ## Common errors and resolutions
  
* **Problem**: You cannot connect to Azure SQL DW using managed identity and ADLS from Databricks, and receive an error message, such as:<br>
  "com.databricks.spark.sqldw.SqlDWSideException: SQL DW failed to execute the JDBC query produced by the connector.
  com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user ‘xxx’. ClientConnectionId: xxx [ErrorCode = 18456] [SQLState = S0001]"
 
  The issue is most likely due to managed identity misconfiguration on Azure SQL DW. 
  
  **Solution**: Follow [steps 1 and 3](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview#steps).
  
* **Problem**: Using Databricks cluster with credential passthrough enabled to access SQL datawarehouse via ODBC results in the error:<br>
  "OperationalError: ('HYT00', '[HYT00] [Microsoft][ODBC Driver 17 for SQL Server]Login timeout expired (0) (SQLDriverConnect)')"."
 
  The pyodbc connection fails because when credential passthrough is enabled on a cluster, the outbound network traffic from Python processes is blocked by design. Also, the SQL database needs some ports to be open, as mentioned in [Ports - ADO.NET](https://docs.microsoft.com/azure/azure-sql/database/adonet-v12-develop-direct-route-ports#inside-client-runs-on-azure).
  
  **Solution**: Provide assignment permissions to the required ports by setting Spark configuration in the cluster, making sure to open ports 1433, and 11000-11999:
  
  ```
  spark.databricks.pyspark.iptable.outbound.whitelisted.ports 1433,11000:11999
  ```

* **Error:** "Remote RPC client disassociated. Likely due to containers exceeding thresholds, or network issues."

  **Solutions**: RPC errors usually occur for the following reasons:
   * The communication between the driver and executor is lost. Executor is not able to send heartbeats within the threshold time frame, which can happen either if the executor is overwhelmed with memory/OOM errors, or too many network hits are making executor too busy in GC and it can't respond to driver.
   In the Spark UI, go to **Stages** and **Sort** tasks based on the error. This will show you which error was happening on the executor level.
   If the current cluster is very small, use a bigger cluster.

  * Having too many partitions. Small files can cause an RPC error. Check the used partition strategy. 

  * Running multiple notebooks on the same cluster can cause issues on the driver. Split the workload across multiple clusters.

  * Implement workload through Azure Firewall to Azure Databricks VNet injected workspace. Make a note of Azure Databricks control plane endpoints for your workspace (map it based on region of your workspace) when configuring Azure Firewall rules:

	|     Name                                                             |     Source                                |     Destination                                                                                                                                                                                                                                 |     Protocol:Port    |     Purpose                                                                                                   |
	|----------------------------------------------------------------------|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|---------------------------------------------------------------------------------------------------------------|
	|     databricks-webapp                                                |     Azure Databricks workspace subnets    |     [Region specific Webapp Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#control-plane-nat-and-webapp-ip-addresses)                                                                |     tcp:443          |     Communication with Azure Databricks webapp                                                                |
	|     databricks-log-blob-storage                                      |     Azure Databricks workspace subnets    |     [Region specific Log Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)         |     https:443        |     To store Azure Databricks audit and cluster logs (anonymized / masked) for support and troubleshooting    |
	|     databricks-artifact-blob-storage                                 |     Azure Databricks workspace subnets    |     [Region specific Artifact Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)    |     https:443        |     Stores Databricks Runtime images to be deployed on cluster nodes                                          |
	|     databricks-dbfs                                                  |     Azure Databricks workspace subnets    |     [DBFS Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#dbfs-root-blob-storage-ip-address)                                                                             |     https:443        |     Azure Databricks workspace root storage                                                                   |
	|     databricks-sql-metastore (OPTIONAL – External Hive Metastore)    |     Azure Databricks workspace subnets    |     [Region specific SQL Metastore Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)            |     tcp:3306         |     Stores metadata for databases and child objects in Azure Databricks workspace                             |


* **Problem:** Network connection error when trying to fetch URL using Scala "javax.net.ssl.SSLException: Connection reset"
  
  1. Run this command in a notebook to create [init script](https://docs.microsoft.com/azure/databricks/clusters/init-scripts):
  
    ```
    dbutils.fs.put("dbfs:/databricks/ssl_change.sh","""
    #!/bin/bash
    echo "jdk.tls.disabledAlgorithms=anon, NULL" > /databricks/spark/dbconf/java/extra.security
    """,True)
    ```
    
  2. [Add init script path to cluster configuration](https://docs.microsoft.com/azure/databricks/clusters/init-scripts#--configure-a-cluster-scoped-init-script):
  
     ```
     dbfs:/databricks/ssl_change.sh
     ```
     
  3. Restart the cluster and test this scala code:
     
     ```
     %scala val html = scala.io.Source.fromURL("https://azure.microsoft.com/api/v2/pricing/databricks/calculator/?currency=US").mkString’
     ```
     
## Unique, per-workspace URLs in Azure Databricks

* Azure Databricks has added a unique URL for each workspace, which uses the following format:

    ```
    adb-<workspace-id>.<random-number>.azuredatabricks.net
    ```

  This URL complements the existing regional URLs (<region>.azuredatabricks.net) you use to access your workspaces. Both URLs will continue to be supported. Because Azure Databricks adds more infrastructure into existing regions, the regional URLs for new workspaces may vary from those of your existing workspaces. We recommend that you use the new per-workspace URL in scripts and in other automation for multiple workspaces. 
  For instructions, see the following:

     - [How do I launch my workspace using the per-workspace URL?](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#launch-a-workspace-using-the-per-workspace-url)
     - [Migrate scripts and other automation](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#migrate-your-scripts-to-use-per-workspace-urls)
     - [Find the regional URL for a workspace](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#find-the-legacy-regional-url-for-a-workspace)

* To run a Spark job, you need at least one worker. If a cluster has zero workers, you can run non-Spark commands on the driver, but Spark commands will fail.

* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Use [user-defined routes](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--step-3-create-user-defined-routes-and-associate-them-with-your-azure-databricks-virtual-network-subnets) to solve this problem.

* Use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. You can use the single IP address as an additional security layer with other Azure services and applications that allow access based on specific IP addresses, by following the instructions in [how to assign a single public IP for VNet-injected workspaces using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip).

* If **IP Access List** is enabled for the workspace, make sure to provide assignment permissions for Azure Data Factory IPs to run notebooks from ADF:

  - To update the IP access list, or to create additional access lists with a new CIDR, see [IP access lists](https://docs.microsoft.com/azure/databricks/security/network/ip-access-list).
  - For information about adding assignment permissions for CIDRs, see [Azure IP Ranges and Service Tags – Public Cloud]( https://www.microsoft.com/download/details.aspx?id=56519) file.  Search for **DataFactory.Region**. 
  
## **Recommended Documents**

* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [Connect your Azure Databricks Workspace to your On-Premises Network](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network)
* [How to Save Plotly Files and Display From DBFS](https://docs.microsoft.com/azure/databricks/kb/visualizations/save-plotly-to-dbfs)
* [Configure custom DNS](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--option-configure-custom-dns) for VNet- injected workspaces
