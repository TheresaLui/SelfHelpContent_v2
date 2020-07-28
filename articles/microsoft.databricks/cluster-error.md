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

| ERROR | RECOMMENDED STEPS|
|-------|---------|
|Error code 500|The error is usually due to transient issues. Please check status pages and try again:<br>[Databricks Status Page](https://status.azuredatabricks.net)<br/>[Azure Status Page](https://status.azure.com/status)|
|Subscription xx was used to perform too many calls within last 5 minutes. The number of calls exceeds Microsoft. Network throttling limit. or Encountered Azure Resource provider throttling. Please try again later.| 1. Use Pool to reduce churn of resources<br>2. Perform cluster creation/resize in smaller batches
|Self-Bootstrap Failure. Node Daemon ping timeout in 600 seconds|Double check UDR configuration as per [this document](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#udr)
|Driver failed to start in time<br>INTERNAL_ERROR: The Spark driver failed to start within 300 seconds<br/>Cluster failed to be healthy within 200 seconds|Store the Hive libraries in DBFS and access them locally from the DBFS location. See [Spark Options](https://docs.microsoft.com/azure/databricks/data/metastores/external-hive-metastore#spark-options)<br>More information on cause of this error [here](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#cluster-timeout)
|The cluster could not be started in 50 minutes. Cause: Timed out with exception after <xx> attempts|Use a [cluster-scoped init script](https://docs.microsoft.com/azure/databricks/clusters/init-scripts#cluster-scoped-init-script) instead of global or cluster-named init scripts. With cluster-scoped init scripts, Azure Databricks does not use synchronous blocking of RPCs to fetch init script execution status<br>More information on cause of this error [here](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#global-or-cluster-specific-init-scripts)
|Library installation timed out after 1800 seconds. Libraries that are not yet installed:xx|Usually you can fix this problem by re-running the job or restarting the cluster.The library installer is configured to time out after 3 minutes. While fetching and installing jars, a timeout can occur due to network problems. To mitigate this issue, you can download the libraries from maven to a DBFS location and install it from there.<br>More information on cause of this error [here](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#too-many-libraries-installed-in-cluster-ui)
|Cluster terminated. Reason: Cloud Provider Limit|See the cloud provider error information in [cluster unexpected termination](https://docs.microsoft.com/azure/databricks/kb/clusters/termination-reasons)
|Cluster terminated. Reason: Cloud Provider Shutdown|See the cloud provider error information in [cluster unexpected termination](https://docs.microsoft.com/azure/databricks/kb/clusters/termination-reasons)
|Cluster terminated. Reason: Instances Unreachable<br>An unexpected error was encountered while setting up the cluster. Please retry and contact Azure Databricks if the problem persists. Internal error message: Timeout while placing node|Add a user-defined route (UDR) to give the Azure Databricks control plane ssh access to the cluster instances, Blob Storage instances, and artifact resources. This custom UDR allows outbound connections and does not interfere with cluster creation. For detailed UDR instructions, see [Step 3: Create user-defined routes and associate them with your Azure Databricks virtual network subnets](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#create-routes). For more VNet-related troubleshooting information, see [Troubleshooting](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject#troubleshooting)<br>More information on cause of this error [here](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable)
|Cloud Provider Launch Failure: A cloud provider error was encountered while setting up the cluster.<br>Operation results in exceeding quota limits of Core. Maximum allowed: xx, Current in use: xxx, Additional requested: xx|Request additional quota as per the article [here](https://docs.microsoft.com/azure/databricks/kb/clusters/azure-core-limit)
|Cloud Provider Launch Failure: A cloud provider error was encountered while setting up the cluster<br>ResourceQuotaExceeded Azure error message: Creating the resource of type 'Microsoft.Network/publicIPAddresses' would exceed the quota of 'xx' resources of type 'Microsoft.Network/publicIPAddresses' per resource group. The current resource count is 'xx', please delete some resources of this type before creating a new one.|Request additional quota as per the article [here](https://docs.microsoft.com/azure/databricks/kb/clusters/azure-ip-limit)



## **Recommended Documents**

> **Known Issue**: Starting 17 June 2020 some Azure Databricks customers in UAE North have encountered error "Azure error code: AllocationFailed" when performing service management operations - such as create, update, scale clusters or submit jobs. We are aware of this issue and are actively working to ensure availability of resources in the quickest time frame possible. We recommend you consider one of the below workarounds:
>
> * Shift the workload towards the end of the working day if possible
> * Try to provision an alternate family VM
> * Increase the size of the VM but provision fewer executors
> * Provision smaller clusters, this increases the chance that enough VMs will be available for your clusters
> * Use pools to reserve instances and configure clusters to use these pools. Please be aware this may increase costs and it’s best if you use this only for essential workloads, if applicable.
> * Deploy the workspace in a different region
>
> If the above workarounds are not viable or did not resolve the issue, please continue with support request creation
>
> Please visit [blog](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/) for more details on our commitment to customers and Microsoft cloud services continuity.
