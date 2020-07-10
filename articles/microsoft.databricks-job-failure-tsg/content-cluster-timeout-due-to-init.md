<properties
	pageTitle="Cluster timeout due to Init"
	description="Cluster timeout due to Init"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="308d49ba-b4b8-4517-acdc-696dfcc56c81"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Cluster timeout due to Init

Cluster startup fails with timeout error: *The cluster could not be started in 50 minutes. Cause: Timed out with exception after <xx> attempts.*

Init scripts that run during the cluster spin-up stage send an RPC (remote procedure call) to each worker machine to run the scripts locally. All RPCs must return their status before the process continues. If any RPC hits an issue and doesn?t respond back (due to a transient networking issue, for example), then the 1-hour timeout can be hit, causing the cluster setup job to fail.

**Troubleshooting and Solution**

1. Validate if customer uses Init script V1 (cluster named or global init scripts).
2. Confirm this is transient issue, check init logs to rule out any issues due to script error.

As a solution, use a [cluster-scoped init script](https://docs.microsoft.com/en-us/azure/databricks/clusters/init-scripts#--cluster-scoped-init-scripts) instead of global or cluster-named init scripts. With cluster-scoped init scripts, Databricks does not use synchronous blocking of RPCs to fetch init script execution status.

If issue persists after trying the suggested approach, please discuss issue further with your SME/TA/EEE using [Ava](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312127/Ava), and [involve Databricks](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312121/Engaging-Databricks-Support) if needed.
