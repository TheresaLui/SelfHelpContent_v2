<properties
	pageTitle="Diagnose and resolve issues with connectivity to Databricks cluster"
	description="Diagnose and resolve issues with connectivity to Databricks cluster"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677672"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="28f97f4f-c4a1-4cd3-81a4-e76d11e147de"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with connectivity to Databricks cluster

## **Recommended Steps**

* The Azure Databricks connector integrated in Power BI Desktop is in [Public Preview](https://powerbi.microsoft.com/blog/announcing-power-bi-connector-to-azure-databricks-public-preview/). Make sure to upgrade Power BI Desktop to version 2.85.681.0 and above to use it.

* If IP Access List feature is enabled for the workspace, make sure to whitelist Azure Data Factory IPs so that you can run notebooks from ADF:

  - To update IP access list or create additional new one with new CIDR, follow [these instructions](https://docs.microsoft.com/azure/databricks/security/network/ip-access-list).
  - See the [Azure IP Ranges and Service Tags – Public Cloud]( https://www.microsoft.com/download/details.aspx?id=56519) file for CIDRs to be whitelisted. Search for DataFactory.Region. 

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* You can use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. The single IP address can be used as an additional security layer with other Azure services and applications that allow access based on specific IP addresses: [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
* You can get the public/private IP address of your [driver or executor node(s)](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/clusters#--sparknode) by running this command in a notebook:

```
	%sh
	curl -H Metadata:true "http://169.254.169.254/metadata/instance/network?api-version=2017-08-01"
```
