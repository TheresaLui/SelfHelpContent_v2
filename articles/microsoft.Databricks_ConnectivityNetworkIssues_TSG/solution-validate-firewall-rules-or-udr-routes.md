<properties
	pageTitle="Validate Firewall rules or UDR routes"
	description="Validate Firewall rules or UDR routes"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ab3ee843-098f-437c-86d4-884485eca2af"
  ownershipId="AzureData_AzureDatabricks"
/>

At this point, we need to validate if firewall rules have route or UDR has route to [all artifacts listed here](https://docs.microsoft.com/en-us/azure/databricks/administration-guide/cloud-configurations/azure/udr). Please double check the configurations and try again. 

**Note:** All artifacts can be added to firewall rules list including webapp except control plane IP. The control plane IP should be added to UDR but adding or whitelisting in firewall is not supported. If you want a solution that requires a compliance that all traffic should be routed via firewall, it is recommended to adopt NPIP solution which facilitates the same. 

**Recommended Documents:**
<br />
* [User-defined route settings for Azure Databricks](https://docs.microsoft.com/en-us/azure/databricks/administration-guide/cloud-configurations/azure/udr)
<br />
* [Secure cluster connectivity (No Public IP / NPIP)](https://docs.microsoft.com/en-us/azure/databricks/security/secure-cluster-connectivity)
