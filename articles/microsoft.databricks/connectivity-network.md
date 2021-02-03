<properties
	pageTitle="Diagnose and resolve connectivity issues with network configuration"
	description="Diagnose and resolve connectivity issues with network configuration"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677711"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="64e0439a-9d7d-40c8-8084-9048d0306b54"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve connectivity issues with network configuration

* The default deployment of Azure Databricks is a fully managed service on Azure. All data plane resources are deployed to a locked resource group. This  includes a VNet that all clusters are associated with. However, if you require network customization, [Deploy Azure Databricks data plane resources in your own virtual network - VNet injection](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject). <br>
   This enables you to:

     - Connect Azure Databricks to other Azure services (such as Azure Storage and EventHubs) in a more secure manner
     - Connect to on-premises data sources taking advantage of user-defined routes
     - Connect Azure Databricks to a network virtual appliance to inspect all outbound traffic, and take actions according to allow and deny rules using user-defined routes
     - Configure Azure Databricks to use custom DNS
     - Configure network security group (NSG) rules to specify egress traffic restrictions
     - Deploy Azure Databricks clusters in your existing VNet

* How To [Establish connectivity from your Azure Databricks workspace to your on-premises network](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network)
     - [Option: Route Azure Databricks traffic using a virtual appliance or firewall](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--option-route-azure-databricks-traffic-using-a-virtual-appliance-or-firewall)
     - [Option: Configure custom DNS](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--option-configure-custom-dns)
     

* Use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. Use the single IP address as an additional security layer with other Azure services and applications that allow access based on specific IP addresses by following the instructions for [how to assign a single public IP for VNet-injected workspaces using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip).

* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Use [user-defined routes](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--step-3-create-user-defined-routes-and-associate-them-with-your-azure-databricks-virtual-network-subnets) to solve this problem.

## **Recommended Steps**

* To run a Spark job, you need at least one worker. If a cluster has zero workers, you can run non-Spark commands on the driver, but Spark commands will fail.

* Implement workloads through Azure Firewall to the Azure Databricks VNet injected workspace. Make a note of Azure Databricks control plane endpoints for your workspace (map it based on region of your workspace) when configuring Azure Firewall rules:


	|     Name                                                             |     Source                                |     Destination                                             |     Protocol:Port    |     Purpose                                                                                                   |
	|----------------------------------------------------------------------|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|---------------------------------------------------------------------------------------------------------------|
	|     databricks-webapp                                                |     Azure Databricks workspace subnets    |     [Region-specific Webapp Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#control-plane-nat-and-webapp-ip-addresses)                                                                |     tcp:443          |     Communication with Azure Databricks webapp                                                                |
	|     databricks-log-blob-storage                                      |     Azure Databricks workspace subnets    |     [Region-specific Log Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)         |     https:443        |     To store Azure Databricks audit and cluster logs (anonymized / masked) for support and troubleshooting    |
	|     databricks-artifact-blob-storage                                 |     Azure Databricks workspace subnets    |     [Region-specific Artifact Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)    |     https:443        |     Stores Databricks Runtime images to be deployed on cluster nodes                                          |
	|     databricks-dbfs                                                  |     Azure Databricks workspace subnets    |     [DBFS Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#dbfs-root-blob-storage-ip-address)                                                                             |     https:443        |     Azure Databricks workspace root storage                                                                   |
	|     databricks-sql-metastore (OPTIONAL – External Hive Metastore)    |     Azure Databricks workspace subnets    |     [Region-specific SQL Metastore Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)            |     tcp:3306         |     Stores metadata for databases and child objects in Azure Databricks workspace                             |


* If **IP Access List** is enabled for the workspace, make sure to assign permissions for Azure Data Factory IPs to run notebooks from ADF:

  - To update the IP access list, or to create access lists with the new CIDR, see this [document](https://docs.microsoft.com/azure/databricks/security/network/ip-access-list).

  - For information about assignment permissions for CIDRs, see [Azure IP Ranges and Service Tags – Public Cloud]( https://www.microsoft.com/download/details.aspx?id=56519).  Search for **DataFactory.Region**. 

* To synchronize workbooks between a local repo like on-premise DevOps instance and a Databricks workspace:

  - You must add the [Webapp IP](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#control-plane-nat-and-webapp-ip-addresses) on the on-premise server to the allow list. 
  - Synchronize notebooks using Workspace CLI or Databricks CLI. [Workspace CLI](https://docs.microsoft.com/azure/databricks/dev-tools/cli/workspace-cli) uses Azure Devops build-and-release pipelines to automate the process. [Databricks CLI](https://docs.microsoft.com/azure/databricks/dev-tools/cli/) provides a more controllable option and can be used to define the workflow to export and import notebooks.
  
## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [A technical overview of Azure Databricks](https://azure.microsoft.com/blog/a-technical-overview-of-azure-databricks/)
* [Virtual Network Peering](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/vnet-peering.html)
* [Configure custom DNS](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--option-configure-custom-dns) for VNet-injected workspaces
