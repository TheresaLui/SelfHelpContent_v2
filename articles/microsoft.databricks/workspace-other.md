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
* In April 2020, Azure Databricks added **a new unique per-workspace URL for each workspace**. This per-workspace URL has the format:

    ```
    adb-<workspace-id>.<random-number>.azuredatabricks.net
    ```

	This URL is complementary to the existing regional URLs (<region>.azuredatabricks.net) that you have used up to now to access your workspaces. Both URLs continue to be supported. However, as Azure Databricks adds more infrastructure into existing regions, the regional URLs for new workspaces may vary from those of your existing workspaces. We therefore strongly recommend that you use the new per-workspace URL in scripts or other automation that you want to use with multiple workspaces.

	* [How do I launch my workspace using the per-workspace URL?](https://docs.microsoft.com/azure/databricks/workspace/migrate-workspace-urls#how-do-i-launch-my-workspace-using-the-per-workspace-url)
	* [Migrate scripts and other automation](https://docs.microsoft.com/azure/databricks/workspace/migrate-workspace-urls#migrate-scripts-and-other-automation)
	* [Find the regional URL for a workspace](https://docs.microsoft.com/azure/databricks/workspace/migrate-workspace-urls#find-the-regional-url-for-a-workspace)	

* [Configure custom DNS](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--option-configure-custom-dns) for VNet injected workspace
* Deploying Azure Databricks data plane resources to your own VNet lets you take advantage of flexible CIDR ranges. If your **current workspace cannot accommodate the required number of active cluster nodes**:

	* You cannot replace the VNet for an existing workspace
	* You cannot change subnet CIDR range for an existing workspace

	Instead, it is recommended that you create another workspace in a larger VNet. Follow these [detailed migration steps](https://docs.microsoft.com/azure/azure-databricks/howto-regional-disaster-recovery#detailed-migration-steps) to copy resources (notebooks, cluster configurations, jobs) from the old to new workspace.	

* [Migrate Azure Databricks workspace between subscriptions or regions](https://docs.microsoft.com/azure/databricks/scenarios/howto-regional-disaster-recovery#detailed-migration-steps). The new workspace should be created first and then migrate all notebooks, jobs configuration, clusters configuration, users, libraries, mounts, init scripts.

* [Migrate production jobs from Apache Spark on other platforms to Apache Spark on Azure Databricks](https://docs.microsoft.com/azure/databricks/migration/production)

* Implement workload through Azure Firewall to Azure Databricks - please take a note of Azure Databricks control plane endpoints for your workspace (map it based on region of your workspace) when configuring Azure Firewall rules:

|     Name                                                             |     Source                                |     Destination                                                                                                                                                                                                                                 |     Protocol:Port    |     Purpose                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|---------------------------------------------------------------------------------------------------------------|
|     databricks-webapp                                                |     Azure Databricks workspace subnets    |     [Region specific Webapp Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#control-plane-nat-and-webapp-ip-addresses)                                                                |     tcp:443          |     Communication with Azure Databricks webapp                                                                |
|     databricks-log-blob-storage                                      |     Azure Databricks workspace subnets    |     [Region specific Log Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)         |     https:443        |     To store Azure Databricks audit and cluster logs (anonymized / masked) for support and troubleshooting    |
|     databricks-artifact-blob-storage                                 |     Azure Databricks workspace subnets    |     [Region specific Artifact Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)    |     https:443        |     Stores Databricks Runtime images to be deployed on cluster nodes                                          |
|     databricks-dbfs                                                  |     Azure Databricks workspace subnets    |     [DBFS Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#dbfs-root-blob-storage-ip-address)                                                                             |     https:443        |     Azure Databricks workspace root storage                                                                   |
|     databricks-sql-metastore (OPTIONAL – External Hive Metastore)    |     Azure Databricks workspace subnets    |     [Region specific SQL Metastore Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)            |     tcp:3306         |     Stores metadata for databases and child objects in Azure Databricks workspace                             |



## **Recommended Documents**

* [Azure Databricks Pricing](https://azure.microsoft.com/pricing/details/databricks/#:~:text=Pay%20as%20you%20go,of%20instance%20running%20Azure%20Databricks.)
* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform
* [Azure Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations.

