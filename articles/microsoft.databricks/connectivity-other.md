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

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [Connect your Azure Databricks Workspace to your On-Premises Network](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network)
* [How to Save Plotly Files and Display From DBFS](https://docs.microsoft.com/azure/databricks/kb/visualizations/save-plotly-to-dbfs)
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Please use [User-defined routes](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--step-3-create-user-defined-routes-and-associate-them-with-your-azure-databricks-virtual-network-subnets) to solve this problem.
* You can use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. The single IP address can be used as an additional security layer with other Azure services and applications that allow access based on specific IP addresses: [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
* In April 2020, Azure Databricks added **a new unique per-workspace URL for each workspace**. This per-workspace URL has the format:

    ```
    adb-<workspace-id>.<random-number>.azuredatabricks.net
    ```

	This URL is complementary to the existing regional URLs (<region>.azuredatabricks.net) that you have used up to now to access your workspaces. Both URLs continue to be supported. However, as Azure Databricks adds more infrastructure into existing regions, the regional URLs for new workspaces may vary from those of your existing workspaces. We therefore strongly recommend that you use the new per-workspace URL in scripts or other automation that you want to use with multiple workspaces.

	* [How do I launch my workspace using the per-workspace URL?](https://docs.microsoft.com/azure/databricks/workspace/migrate-workspace-urls#how-do-i-launch-my-workspace-using-the-per-workspace-url)
	* [Migrate scripts and other automation](https://docs.microsoft.com/azure/databricks/workspace/migrate-workspace-urls#migrate-scripts-and-other-automation)
	* [Find the regional URL for a workspace](https://docs.microsoft.com/azure/databricks/workspace/migrate-workspace-urls#find-the-regional-url-for-a-workspace)

* You can use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. The single IP address can be used as an additional security layer with other Azure services and applications that allow access based on specific IP addresses: [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)

* [Configure custom DNS](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--option-configure-custom-dns) for VNet injected workspace

