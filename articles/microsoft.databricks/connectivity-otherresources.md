<properties
	pageTitle="Diagnose and resolve connectivity issues to other resources"
	description="Diagnose and resolve connectivity issues to other resources"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677674"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e5d3f19b-7f84-4355-81c3-1b2eb064c282"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve connectivity issues

## **Recommended Steps**

* **Azure Event Hubs + Apache Spark connector** is updated regularly, and a more recent version may be available. We recommend that you [pull the latest connector from the Maven repository](https://mvnrepository.com/artifact/com.microsoft.azure/azure-eventhubs-spark).

* If the IP Access List feature is enabled for the workspace, make sure to provide assignment permissions to Azure Data Factory IPs so that you can run notebooks from ADF:

  - To update the IP access list or create a new one with a new CIDR, follow [these instructions](https://docs.microsoft.com/azure/databricks/security/network/ip-access-list)
  - For CIDRs that need assignment permissions, see [Azure IP Ranges and Service Tags – Public Cloud]( https://www.microsoft.com/download/details.aspx?id=56519), and search for **DataFactory.Region** 
  
* To synchronize workbooks between a local repo like on-premise DevOps instance and a Databricks workspace:

  - Add the [Webapp IP](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#control-plane-nat-and-webapp-ip-addresses) on the on-premise server to the **Allow list**. 
  - Use one of the following options to synchronize notebooks: [Workspace CLI](https://docs.microsoft.com/azure/databricks/dev-tools/cli/workspace-cli) uses Azure Devops build and release pipelines to automate the process; [Databricks CLI](https://docs.microsoft.com/azure/databricks/dev-tools/cli/) provides a more controllable approach by letting you define the workflow to export and import notebooks.

## **Recommended Documents**

* [How To: Connect to Azure Synapse Analytics](https://docs.microsoft.com/azure/databricks/data/data-sources/azure/synapse-analytics)
* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Connect your Azure Databricks Workspace to your On-Premises Network](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network)
* [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
