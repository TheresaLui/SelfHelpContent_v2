<properties
	pageTitle="Troubleshooting"
	description="Troubleshooting"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ae5493cd-143c-4651-9b2e-b18214684917"
  ownershipId="AzureData_AzureDatabricks"
/>

## Validate the following:

<br />
**1. Is issue reproducible for specific cluster(s)?**

- Check if any init script added to failing cluster(s).
- Collect cluster URL, init script name with complete path, and error with which init script/cluster creation fails.
- Refer to [this TSG](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/314113/Common-Solutions) to further TS the init script issue.


**2. Validate if firewall rules have route or UDR has route to [all artifacts listed in this document](https://docs.microsoft.com/en-us/azure/databricks/administration-guide/cloud-configurations/azure/udr).** 
  
**Note:** All artifacts can be added to firewall rules list including webapp except control plane IP. The control plane IP should be added to UDR but adding or whitelisting in firewall is not supported. If the customer wants a solution that requires a compliance that all traffic should be routed via firewall, they should adopt [NPIP solution](https://docs.microsoft.com/en-us/azure/databricks/security/secure-cluster-connectivity) which facilitates the same. 

**3. Databricks requires default mandatory NSG rules as prescribed [here](https://docs.microsoft.com/en-us/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject#nsg).** Missing any of them will lead to failure. 

<br />
**Next Steps:**

* If issue is caused by init script, please follow the TSG mentioned above in (1)
* If it is related to (2) or (3), please proceed to customer ready content
* Otherwise, involve SME through AVA for further assistance
