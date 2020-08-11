<properties
	pageTitle="NRP Throttling Issue"
	description="NRP Throttling Issue"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="0b1b9777-f29c-4c2e-b8b8-106bb4283ea4"
   	ownershipId="AzureData_AzureDatabricks"
/>

# NRP Throttling Issue

This usually occurs when there is about 50 simultaneous write operations (create/delete) on public IPs in a given subscription which creates a slowdown on NRP operations and induces throttling, and results in all the requests above the limit failures. 

**User facing Error:** *Subscription XXX was used to perform too many calls within last 5 minutes. The number of calls exceeds Microsoft. Network throttling limit. or Encountered Azure Resource provider throttling. Please try again later.*

## Troubleshooting and Solution

1. Check number of nodes requested for cluster creation and see if multiple clusters are being spun up and terminated
2. Check if this Subscription has multiple workspaces created
3. Check cluster events tab for cluster creation failure/delay cases
4. Check driver logs for job failure cases

Good solution to this problem would be to use [Pools](https://docs.microsoft.com/azure/databricks/clusters/instance-pools/) to reduce churn of resources.

Another suggested workaround is to perform resizing and/or create clusters in smaller batches (around 50 workers max at one time). This number can also be affected by whatever else is occurring in the customer subscription since the throttling is occurring at the subscription level (whether databricks or non-databricks related Azure events).

Provide customer with ready message below, and if issue persists after trying the suggested approach, please discuss issue further with your SME/TA/EEE using [Ava](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312127/Ava), and [file an IcM](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/333941/Escalate-to-Product-Group-team) if needed.
