<properties
	pageTitle="Diagnose and resolve cluster launch or create errors"
	description="Diagnose and resolve cluster launch or create errors"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32745366"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e6779765-0078-41c2-85d1-99dbb3dd579b"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve cluster create and launch errors

First, review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes.

## **Recommended Steps**

* Find a list of supported instance/node types [Pricing page under Instances section](https://azure.microsoft.com/pricing/details/databricks/).

* Review important details for [VNet Injected workspace](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject):
   
   * Deploying Azure Databricks data plane resources to your own VNet lets you take advantage of flexible CIDR ranges (anywhere between /16-/24 for the VNet and up to /26 for the subnets).
   
   * You cannot replace the VNet for an existing workspace or modify the subnet CIDR ranges. If your current workspace cannot accommodate the required number of active cluster nodes, we recommend that you create another workspace in a larger VNet. Follow these [detailed migration steps](https://docs.microsoft.com/azure/databricks/scenarios/howto-regional-disaster-recovery#detailed-migration-steps) to copy resources (notebooks, cluster configurations, jobs) from the old to new workspace.
   
* **Common Errors**

| ERROR | RECOMMENDED STEPS|
|-------|---------|
|Error code 500|The error is usually due to transient issues. Check status pages and try again:<br>[Databricks status page](https://status.azuredatabricks.net)<br/>[Azure status page](https://status.azure.com/status)|
|Subscription xx was used to perform too many calls within last 5 minutes. The number of calls exceeds Microsoft Network throttling limit or Encountered Azure Resource provider throttling. Try again later.| 1. Use Pool to reduce churn of resources<br>2. Perform cluster creation/resize in smaller batches
|Self-Bootstrap Failure. Node Daemon ping timeout in 600 seconds | Double-check UDR configuration as described in [this document](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#udr)
|Timeout after xxx milliseconds with threshold 600 seconds. Check network connectivity from data plane to control plane. | Make sure to add the UDR to the control plane. Double-check UDR configuration as described in [this document](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#udr).
|Driver failed to start in time<br>INTERNAL_ERROR: The Spark driver failed to start within 300 seconds<br/>Cluster failed to be healthy within 200 seconds|Store the Hive libraries in DBFS and access them locally from the DBFS location. See [Spark options](https://docs.microsoft.com/azure/databricks/data/metastores/external-hive-metastore#spark-options).<br>See [more information about the cause of this error](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#cluster-timeout).
|The cluster could not be started in 50 minutes. Cause: Timed out with exception after <xx> attempts|Use a [cluster-scoped init script](https://docs.microsoft.com/azure/databricks/clusters/init-scripts#cluster-scoped-init-script) instead of global or cluster-named init scripts. With cluster-scoped init scripts, Azure Databricks does not use synchronous blocking of RPCs to fetch init script execution status.<br>See [more information about the cause of this error](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#global-or-cluster-specific-init-scripts).
|Library installation timed out after 1800 seconds. Libraries that are not yet installed:xx|Usually you can fix this problem by running the job again or restarting the cluster.The library installer is configured to time out after 3 minutes. While fetching and installing jars, a timeout can occur due to network problems. To mitigate this issue, download the libraries from maven to a DBFS location and install it from there.<br>More information [about the cause of this error](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#too-many-libraries-installed-in-cluster-ui).
|Cluster terminated. Reason: Cloud Provider Limit|See the cloud provider error information in [cluster unexpected termination](https://docs.microsoft.com/azure/databricks/kb/clusters/termination-reasons)
|Cluster terminated. Reason: Cloud Provider Shutdown|See the cloud provider error information in [cluster unexpected termination](https://docs.microsoft.com/azure/databricks/kb/clusters/termination-reasons)
|Cluster terminated. Reason: Instances Unreachable<br>An unexpected error was encountered while setting up the cluster. Retry and contact Azure Databricks if the problem persists. Internal error message: Timeout while placing node|Add a user-defined route (UDR) to give the Azure Databricks control plane ssh access to the cluster instances, Blob Storage instances, and artifact resources. This custom UDR allows outbound connections and does not interfere with cluster creation. For detailed UDR instructions, see [Step 3: Create user-defined routes and associate them with your Azure Databricks virtual network subnets](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#create-routes). For more VNet-related troubleshooting information, see [Troubleshooting](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject#troubleshooting).<br>More information on cause of this error [here](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable).
|Cloud Provider Launch Failure: A cloud provider error was encountered while setting up the cluster.<br>Operation results in exceeding quota limits of Core. Maximum allowed: xx, Current in use: xxx, Additional requested: xx|Request additional quota, as described in [this article](https://docs.microsoft.com/azure/databricks/kb/clusters/azure-core-limit)
|Cloud Provider Launch Failure: A cloud provider error was encountered while setting up the cluster<br>ResourceQuotaExceeded Azure error message: Creating the resource of type `Microsoft.Network/publicIPAddresses` would exceed the quota of "xx" resources of type `Microsoft.Network/publicIPAddresses` per resource group. The current resource count is "xx". Delete some resources of this type before creating a new one.|Request additional quota, as described in [this article](https://docs.microsoft.com/azure/databricks/kb/clusters/azure-ip-limit).




