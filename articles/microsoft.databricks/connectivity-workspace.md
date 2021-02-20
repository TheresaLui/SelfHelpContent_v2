<properties
	pageTitle="Diagnose and resolve issues with connectivity to workspace"
	description="Diagnose and resolve issues with connectivity to Workspace"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677673"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b0d6610b-0a52-4891-a974-0fdd2f4ce176"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with connectivity to Workspace

> **Check [Azure Databricks status page](https://status.azuredatabricks.net/) for current status by region. We highly recommended subscribing for updates on this page, which will automatically notify you of future status changes.**

## **Recommended Steps**

### **Troubleshooting Errors**

* When signing in to Workspace, you receive this error: 

  ```
  We’ve encountered an error logging you in. Databricks support has been alerted and will begin looking into the issue right away. 
  ```
  The workaround is to open a new tab in Google Chrome, or close the browser and erase its history. If this doesn't help, there may be ongoing maintenance or outages. Check the  [Databricks status page](https://status.azuredatabricks.net/) to confirm.
  
* Learn how to resolve errors for [instances unreachable](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable)

### **Configuration and Setup**

* Learn about [workspace access control](https://docs.microsoft.com/azure/databricks/administration-guide/access-control/workspace-acl)
* Learn how to [deploy Azure Databricks in your Azure Virtual Network (VNet injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject). Note that SSH can be enabled only if your workspace is deployed in your own Azure virual network. 
* Learn how to [use the Resource Manager template to create Azure Workspace](https://docs.microsoft.com/azure/azure-databricks/quickstart-create-databricks-workspace-resource-manager-template)
* Learn about [Virtual Network Peering](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-peering)
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. To resolve this issue, use [user-defined routes](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--step-3-create-user-defined-routes-and-associate-them-with-your-azure-databricks-virtual-network-subnets).
* Use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. You can use the single IP address as an additional security layer with other Azure services and applications that allow access based on specific IP addresses, by following the instructions in [how to assign a single public IP for VNet-injected workspaces using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip).
* Get the public/private IP address of your [driver or executor node(s)](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/clusters#--sparknode) by running this command in a notebook:

    ```
    %sh
    curl -H Metadata:true "http://169.254.169.254/metadata/instance/network?api-version=2017-08-01"
    ```
* If IP Access List feature is enabled for the workspace, make sure to whitelist Azure Data Factory IPs to be able to run notebooks from ADF:

  - To update IP access list or create additional new one with new CIDR, please follow this [document](https://docs.microsoft.com/azure/databricks/security/network/ip-access-list).

  - And you can refer to this [Azure IP Ranges and Service Tags – Public Cloud]( https://www.microsoft.com/download/details.aspx?id=56519) file for CIDRs to be whitelisted.  Search for "DataFactory.Region." 
  
* Implement workloads through Azure Firewall to Azure Databricks VNet injected workspace. Make a note of Azure Databricks control plane endpoints for your workspace (map it based on region of your workspace) when configuring Azure Firewall rules:

  |     Name                                                             |     Source                                |     Destination                                                                                                                                                                                                                                 |     Protocol:Port    |     Purpose                                                                                                   |
  |----------------------------------------------------------------------|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|---------------------------------------------------------------------------------------------------------------|
  |     databricks-webapp                                                |     Azure Databricks workspace subnets    |     [Region specific Webapp Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#control-plane-nat-and-webapp-ip-addresses)                                                                |     tcp:443          |     Communication with Azure Databricks webapp                                                                |
  |     databricks-log-blob-storage                                      |     Azure Databricks workspace subnets    |     [Region specific Log Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)         |     https:443        |     To store Azure Databricks audit and cluster logs (anonymized / masked) for support and troubleshooting    |
  |     databricks-artifact-blob-storage                                 |     Azure Databricks workspace subnets    |     [Region specific Artifact Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)    |     https:443        |     Stores Databricks Runtime images to be deployed on cluster nodes                                          |
  |     databricks-dbfs                                                  |     Azure Databricks workspace subnets    |     [DBFS Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#dbfs-root-blob-storage-ip-address)                                                                             |     https:443        |     Azure Databricks workspace root storage                                                                   |
  |     databricks-sql-metastore (OPTIONAL – External Hive Metastore)    |     Azure Databricks workspace subnets    |     [Region specific SQL Metastore Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)            |     tcp:3306         |     Stores metadata for databases and child objects in Azure Databricks workspace                             |


* In April 2020, Azure Databricks added **a new unique per-workspace URL for each workspace**. This per-workspace URL has the following format:

    ```
    adb-<workspace-id>.<random-number>.azuredatabricks.net
    ```

	This URL is complementary to the existing regional URLs (<region>.azuredatabricks.net) that you have used until now to access your workspaces. Both URLs continue to be supported. However, because Azure Databricks adds more infrastructure into existing regions, the regional URLs for new workspaces may vary from those of your existing workspaces. Therefore, we strongly recommend that you **use the new per-workspace URL in scripts or other automation that you want to use with multiple workspaces** by following the instructions in the links below:

	* [How do I launch my workspace using the per-workspace URL?](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#launch-a-workspace-using-the-per-workspace-url)
	* [Migrate scripts and other automation](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#migrate-your-scripts-to-use-per-workspace-urls)
	* [Find the regional URL for a workspace](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#find-the-legacy-regional-url-for-a-workspace)
	


