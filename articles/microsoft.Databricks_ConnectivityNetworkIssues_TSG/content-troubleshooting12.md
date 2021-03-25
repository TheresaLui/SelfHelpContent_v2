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
	articleId="e3913dda-6cfa-4f59-9f7d-f34da2a6b634"
  ownershipId="AzureData_AzureDatabricks"
/>

### Validate the following:
<br />

**1. Is databricks Vnet whitelisted in the firewall of storage?**

   If the firewall does not have databricks VNET whitelisted,whitelist and try.

**2. Does the SP or key have correct credentials?** 

   If the error states the storage has no enough permissions - check the SP or key credentials and make sure it has contributor or full permission over storage account. 

**3. If the storage is using SP or any AD based authentication, it needs AD endpoint enabled.** 

   If  storage has all needed permissions and routes, but notebook keeps running with no error, it should be using  authentication method that needs AD access. Enable AD endpoint on both Databricks subnets and retry.

**4. If issues persist, enable diagnostics logs from storage firewall and capture the IP that is making the call to storage.**

<br />

### Next Steps:
If root cause is one of the mentioned scenarios, please proceed to customer ready content below.
If issue persists, ask SMEs on Ava and involve Storage team if needed.
