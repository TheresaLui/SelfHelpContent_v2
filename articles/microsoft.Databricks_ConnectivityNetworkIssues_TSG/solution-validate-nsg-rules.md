<properties
	pageTitle="Validate NSG Rules"
	description="Validate NSG Rules"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="de193af0-4a17-4b29-b18f-cd062b228f85"
  ownershipId="AzureData_AzureDatabricks"
/>

At this point, we need to validate NSG rules as Databricks requires default mandatory NSG rules; missing any of them will lead to failure. Please compare NSG with your setup [as listed here](as prescribed here: https://docs.microsoft.com/en-us/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject#nsg) and try again. 
