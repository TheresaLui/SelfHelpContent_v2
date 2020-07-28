<properties
	pageTitle="Quota Limit Reached"
	description="Quota Limit Reached"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="732262f9-9ef5-49f8-8fde-38b80b140769"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Quota limit reached (cores, public IPs,...) issue 

<!--issueDescription-->

We have accessed your workspace and cluster event logs, and it seems that cluster launch is failing due to Databricks not being able to acquire VMs getting this error:

*** please paste the error here ***

To resolve the issue:
1. You can either *stop unused clusters* to release resources
2. Or if the first suggested solution is not feasible, please *open a case with Azure Subscription Management team* making sure to incluse these details: 
   Subscription ID, Region, VM type, Current available number of cores, Number of cores to be added
   
## Recommended Documents 
* [Step by step on opening the case](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests)
* [Check resource usage against limits](https://docs.microsoft.com/azure/networking/check-usage-against-limits)

<!--/issueDescription-->