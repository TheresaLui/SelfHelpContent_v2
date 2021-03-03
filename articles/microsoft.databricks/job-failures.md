<properties
	pageTitle="Diagnose and resolve job failures"
	description="Diagnose and resolve job failures"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677702"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="f951a9e3-02de-4747-8f14-e7c8fc1537ae"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve job failures

## **Recommended Steps**

* To run a Spark job, you need at least one worker. If a cluster has zero workers, you can run non-Spark commands on the driver, but Spark commands will fail.

**Error**: Driver failed to start in time. INTERNAL_ERROR: The Spark driver failed to start within 300 seconds; Cluster failed to be healthy within 200 seconds  
* Store the Hive libraries in DBFS and access them locally from the DBFS location. See [Spark Options](https://docs.microsoft.com/azure/databricks/data/metastores/external-hive-metastore#spark-options). More information on this error: [Cluster Timeout](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#cluster-timeout)

**Error**: The cluster could not be started in 50 minutes. Cause: Timed out with exception after <xxx> attempts
* Use a [cluster-scoped init script](https://docs.microsoft.com/azure/databricks/clusters/init-scripts#cluster-scoped-init-script) instead of global or cluster-named init scripts. With cluster-scoped init scripts, Azure Databricks does not use synchronous blocking of RPCs to fetch init script execution status. More information [here](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#global-or-cluster-specific-init-scripts)

**Error**: Library installation timed out after 1800 seconds. 
* Usually you can fix this problem by re-running the job or restarting the cluster. The library installer is configured to time out after 3 minutes. While fetching and installing jars, a timeout can occur due to network problems. To mitigate this issue, you can download the libraries from maven to a DBFS location and install it from there. More information [here](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#too-many-libraries-installed-in-cluster-ui)

**Error**: Cluster terminated. Reason: Cloud Provider Limit
* See the cloud provider error information in [Cluster Unexpected Termination](https://docs.microsoft.com/azure/databricks/kb/clusters/termination-reasons) 

**Error**: Cluster terminated. Reason: Cloud Provider Shutdown
* See the cloud provider error information in [Cluster Unexpected Termination](https://docs.microsoft.com/azure/databricks/kb/clusters/termination-reasons) 

**Error**: Cluster terminated. Reason: Instances Unreachable. An unexpected error was encountered while setting up the cluster.
* Add a user-defined route (UDR) to give the Azure Databricks control plane ssh access to the cluster instances, Blob Storage instances, and artifact resources. This custom UDR allows outbound connections and does not interfere with cluster creation. For detailed UDR instructions, see [Step 3: Create user-defined routes and associate them with your Azure Databricks virtual network subnets](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#create-routes). For more VNet-related troubleshooting information, see [Troubleshooting](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject#troubleshooting). More information on cause of this error [here](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable)

**Error**: Lost connection to cluster. The notebook may have been detached.  Driver is temporarily unavailable.
* Troubleshoot this error according to the steps in [Spark job fails with Driver is temporarily unavailable](https://docs.microsoft.com/azure/databricks/kb/jobs/driver-unavailable)

**Error** : {"error_code":"INVALID_STATE","message":"There were already 1000 jobs created in past 3600 seconds, exceeding rate limit: 1000 job creations per 3600 seconds."}
* Troubleshoot the error according to [Job fails due to job rate limit](https://docs.microsoft.com/azure/databricks/kb/jobs/job-rate-limit)

**Error** : Job stage failures getting org.apache.spark.shuffle.FetchFailedException
* Change shuffle partition configuration at notebook level for this job: spark.conf.set("spark.sql.shuffle.partitions","number_of_partitions")
* Or increase executor(s) memory by upgrading cluster

 * Monitoring [Driver node](https://docs.microsoft.com/azure/databricks/clusters/configure#driver-node) performance:
    * [Ganglia metrics](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#ganglia-metrics)
    * [Diagnostic logging in Azure Databricks](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/azure-diagnostic-logs) - you can stream the VM's metrics to Azure Log Analytics Workspace by installing the Log Analytics Agent on each cluster node.
    **Note:** This could increase cluster startup time by a few minutes.
    * [SSH to Driver on VNet injected workspace](https://docs.microsoft.com/azure/databricks/clusters/configure#--ssh-access-to-clusters) and run bash commands

**Error** : ADF Error code 3204 - ModuleNotFoundError: No module named 'azure'

  * If the job requires certain libraries, make sure to [attach the libraries as dependent libraries within job itself](https://docs.microsoft.com/azure/databricks/kb/jobs/job-fails-no-library)
    
  * [Set library dependencies directly in ADF notebook run](https://docs.microsoft.com/azure/data-factory/transform-data-databricks-notebook#databricks-notebook-activity-properties)
    
  * Apply retry logic by modifying [activity configuration](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities#activity-policy-json-definition) 
  
**Error**:   Remote RPC client disassociated. Likely due to containers exceeding thresholds, or network issues.

  * We generally get RPC error due to the following reasons:

    1. The communication between the driver and executor is lost - executor is not able to send heartbeats within the threshold time frame which can happen either if the executor is overwhelmed with memory/OOM errors or too many network hits are making executor too busy in GC and it is not able to respond back to driver.

       You can see what is happening in the Spark UI > Stages > sort the tasks based on the error. It will show you what error was happening on executor level.

       One quick workaround: use a bigger cluster (if the current cluster is very small).

    2. Having too many partitions - small files can cause RPC error. You can check the used partition strategy.

    3. Running multiple notebooks on the same cluster can sometimes cause issues on the driver. If that is the case, split the workload across multiple clusters.
    
## **Recommended Documents**

* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform
* [Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations.
