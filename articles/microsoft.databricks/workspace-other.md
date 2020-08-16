<properties
	pageTitle="Diagnose and resolve issues with Workspace"
	description="Diagnose and resolve issues with Workspace"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677733"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="32507757-3fe2-45eb-9f0f-fd046dd47472"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Workspace

## **Recommended Steps**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes

* If you are unable to launch or access Azure Databricks workspace due to error "User does not have Contributor or Owner role", the issue is by design. Enable access to users by modifying IAM roles and assign **Contributor** or **Owner** role following steps [here](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/account#--assign-account-admins). User should be added **individually** as adding AD group is *not supported* yet.

* [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
* [Managed Applications and Locks](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources#managed-applications-and-locks)

* Deployment of workspace through ARM Templates fails if you use existing resource group name as a managed resource group. Always ensure [Managed Resource group](https://docs.microsoft.com/azure/managed-applications/overview#managed-resource-group) in ARM template doesn't already exist within the subscription.

* Please avoid having any special characters (- or _) as the first or last character in workspace name. Maximum length for Managed resource group Name: 90 characters. Workspace creation will fail due to invalid characters. 

* [Error: Instances unreachable](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable)
* You can get the public/private IP address of your [driver or executor node(s)](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/clusters#--sparknode) by running this command in a Databricks notebook:

```
    %sh
    curl -H Metadata:true "http://169.254.169.254/metadata/instance/network?api-version=2017-08-01"
```

* [Retrieve the current username for the notebook](https://docs.microsoft.com/azure/databricks/kb/notebooks/get-notebook-username). This is currently supported for:

	* Standard clusters in both Scala and Python
	* High Concurrency clusters in Python with Credential Passthrough **disabled**
	
* Getting error **Unexpected error while loading Spark UI: Max Response Size Reached**: the issue is due to response limit of 30 MB for Spark UI proxy. This can happen if the jobs page returned by Spark UI is very big which can happen in long running cluster with too many jobs. To resolve the issue, please modify [Spark UI configurations](http://spark.apache.org/docs/latest/configuration.html#spark-ui) as below:

```
    spark.ui.retainedJobs 100
    spark.ui.retainedStages 100
    spark.ui.retainedTasks 10000
 ```
 
* Deploying Azure Databricks data plane resources to your own VNet lets you take advantage of flexible CIDR ranges. If your **current workspace cannot accommodate the required number of active cluster nodes**:

	* You cannot replace the VNet for an existing workspace.  
	* You cannot change subnet CIDR range for an existing workspace.

	Instead, it is recommended that you create another workspace in a larger VNet. Follow these [detailed migration steps](https://docs.microsoft.com/azure/azure-databricks/howto-regional-disaster-recovery#detailed-migration-steps) to copy resources (notebooks, cluster configurations, jobs) from the old to new workspace.	


