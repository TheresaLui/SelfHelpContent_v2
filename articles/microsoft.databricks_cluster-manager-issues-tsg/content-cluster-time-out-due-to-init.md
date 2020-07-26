<properties
	pageTitle="Cluster Timeout due to Init Script"
	description="Cluster Timeout due to Init Script"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="5a37e257-9f10-4200-9717-845b60a19239"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Cluster timeout due to init script issue

Cluster startup fails with timeout error: *The cluster could not be started in 50 minutes. Cause: Timed out with exception after <xx> attempts.*

Init scripts that run during the cluster spin-up stage send an RPC (remote procedure call) to each worker machine to run the scripts locally. All RPCs must return their status before the process continues. If any RPC hits an issue and doesn’t respond back (due to a transient networking issue, for example), then the 1-hour timeout can be hit, causing the cluster setup job to fail.

## Troubleshooting and Solution

1. Validate if customer uses Init script V1 (cluster named or global init scripts)
2. Confirm this is transient issue, check init logs to rule out any issues due to script error.

As a solution, use a [cluster-scoped init script](https://docs.microsoft.com/en-us/azure/databricks/clusters/init-scripts#--cluster-scoped-init-scripts) instead of global or cluster-named init scripts. With cluster-scoped init scripts, Databricks does not use synchronous blocking of RPCs to fetch init script execution status.

If issue persists after trying the suggested approach, please discuss issue further with your SME/TA/EEE using [Ava](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312127/Ava), and [involve Databricks](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312121/Engaging-Databricks-Support) if needed.
