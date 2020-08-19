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

**Error**:  Driver failed to start in time. INTERNAL_ERROR: The Spark driver failed to start within 300 seconds; Cluster failed to be healthy within 200 seconds  
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

**Error**: Lost connection to cluster. The notebook may have been detached  
	   Driver is temporarily unavailable
* Troubleshoot this error according to the steps in the article: [Spark job fails with Driver is temporarily unavailable](https://docs.microsoft.com/azure/databricks/kb/jobs/driver-unavailable)

**Error** : {"error_code":"INVALID_STATE","message":"There were already 1000 jobs created in past 3600 seconds, exceeding rate limit: 1000 job creations per 3600 seconds."}
* Troubleshoot the error according to the article: [Job fails due to job rate limit](https://docs.microsoft.com/azure/databricks/kb/jobs/job-rate-limit)
	   

## **Recommended Steps**

When using JAR based jobs on interactive clusters, the JAR jobs will not be automatically updated when a new JAR is uploaded as it will pick up the old JAR. This issue is by design. As a resolution:
* The cluster needs to be restarted whenever you want to update the JAR in the same job
* Or create a new job with same configurations and use the new JAR instead
