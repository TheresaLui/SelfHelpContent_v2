<properties
	pageTitle="Enable AD Endpoint"
	description="Enable AD Endpoint"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="73039b76-c700-43fc-82d4-23fc2d438d82"
  ownershipId="AzureData_AzureDatabricks"
/>

If  Storage has all needed permissions, routes, and correct credentials but notebook keeps running with no error, it should be using  autherntication method that needs AD access. Please enbale AD endpoint on both Databricks subnets and try again.

**Recommended Documents:**
<br />
* [VNet injection](https://docs.microsoft.com/en-us/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
<br />
* [Virtual Network service endpoints](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-service-endpoints-overview)
