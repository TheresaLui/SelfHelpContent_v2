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

Most users can diagnose and resolve issues with Azure Databricks workspace by using the following information.

## **Recommended Steps**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* If you are unable to launch or access Azure Databricks workspace and you receive the error message, "User does not have Contributor or Owner role," the issue is by design. Enable access to users by modifying IAM roles and assign **Contributor** or **Owner** roles by following [these steps](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/account#--assign-account-admins). The user should be added **individually** because adding an AD group is **not supported** yet.

* Login issue getting error: 

  ```
  We’ve encountered an error logging you in. Databricks support has been alerted and will begin looking into the issue right away. 
  ```
 
  To work around this issue, either open a new tab in Google Chrome or close the browser and erase its history. If this doesn't help, there is likely an ongoing maintenance or outages. Check [Databricks status page](https://status.azuredatabricks.net/) to confirm.
 
* When using Azure Databricks, it can be confusing when a new workspace and managed resource group just appear. Azure automatically creates a **Databricks workspace**, as well as a **managed resource group (databricks-rg-xxx-xxx)** containing all the resources needed to run the cluster. 

  This managed resource group (MRG) is protected by a system-level lock to prevent deletions and modifications. The only way to directly remove the lock is to delete the service. However, by making changes to the parent resource group, those changes will be correspondingly updated in the managed resource group.
  
 
* Learn [how to assign a single public IP for VNet-injected workspaces using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
* Learn about [managed applications and locks](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources#managed-applications-and-locks)
* Deploying workspace through ARM Templates will fail if you use existing an resource group name as a managed resource group. Ensure that the [Managed Resource group](https://docs.microsoft.com/azure/managed-applications/overview#managed-resource-group) in the ARM template doesn't already exist within the subscription.
* Avoid having any special characters as the first or last character in a workspace name. The maximum length for a Managed Resource group name is 90 characters. **Invalid characters will cause the workspace creation to fail**. 
* Learn about the ["instances unreachable" error](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable)
* Get the public/private IP address of your [driver or executor node(s)](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/clusters#--sparknode) by running this command in a Databricks notebook:

    ```
    %sh
    curl -H Metadata:true "http://169.254.169.254/metadata/instance/network?api-version=2017-08-01"
    ```
* [Retrieve the current username for the notebook](https://docs.microsoft.com/azure/databricks/kb/notebooks/get-notebook-username). This is supported for:

	* Standard clusters in both Scala and Python
	* High Concurrency clusters in Python with Credential Passthrough **disabled**
	
* If you receive the error message `Unexpected error while loading Spark UI: Max Response Size Reached, the response limit of 30 MB for the Spark UI proxy has been reached`. This can happen if the jobs page returned by the Spark UI is very big, which can happen in a long-running cluster with too many jobs. To resolve the issue, modify [Spark UI configurations](http://spark.apache.org/docs/latest/configuration.html#spark-ui) by running the following command:

    ```
    spark.ui.retainedJobs 100
    spark.ui.retainedStages 100
    spark.ui.retainedTasks 10000
    ```
* In April 2020, Azure Databricks added **a new unique per-workspace URL for each workspace**. This per-workspace URL has the following format: `adb-<workspace-id>.<random-number>.azuredatabricks.net`. This per-workspace URL is complementary to the existing regional URLs (<region>.azuredatabricks.net) that you have used up until now to access your workspaces. Both URLs continue to be supported. However, because Azure Databricks adds more infrastructure into existing regions, the regional URLs for new workspaces may vary from those of your existing workspaces. Therefore, **we strongly recommend that you use the new per-workspace URL in scripts or other automation that you want to use with multiple workspaces**. Follow the instructions in the links below:

	* [How do I launch my workspace using the per-workspace URL?](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#launch-a-workspace-using-the-per-workspace-url)
	* [Migrate scripts and other automation](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#migrate-your-scripts-to-use-per-workspace-urls)
	* [Find the regional URL for a workspace](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#find-the-legacy-regional-url-for-a-workspace)	

* [Configure custom DNS](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--option-configure-custom-dns) for VNet- injected workspaces
* Deploying Azure Databricks data plane resources to your own VNet lets you take advantage of flexible CIDR ranges. If your **current workspace cannot accommodate the required number of active cluster nodes**:

    * You cannot replace the VNet for an existing workspace
    * You cannot change subnet CIDR range for an existing workspace

	Instead, we recommend that you create another workspace in a larger VNet. Follow these [detailed migration steps](https://docs.microsoft.com/azure/azure-databricks/howto-regional-disaster-recovery#detailed-migration-steps) to copy resources (notebooks, cluster configurations, jobs) from the old workspace to the new one.	

* Learn how to [migrate Azure Databricks workspace between subscriptions or regions](https://docs.microsoft.com/azure/databricks/scenarios/howto-regional-disaster-recovery#detailed-migration-steps). Create the new workspace first, and then migrate all notebooks, jobs configuration, clusters configuration, users, libraries, mounts, and init scripts.

* Learn how to [migrate production jobs from Apache Spark on other platforms to Apache Spark on Azure Databricks](https://docs.microsoft.com/azure/databricks/migration/production)

* Implement workload through Azure Firewall to Azure Databricks. Note the Databricks control plane endpoints for your workspace (map them based on the region of your workspace) when configuring Azure Firewall rules:

	|     Name                                                             |     Source                                |     Destination                                                                                                                                                                                                                                 |     Protocol:Port    |     Purpose                                                                                                   |
	|----------------------------------------------------------------------|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|---------------------------------------------------------------------------------------------------------------|
	|     databricks-webapp                                                |     Azure Databricks workspace subnets    |     [Region specific Webapp Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#control-plane-nat-and-webapp-ip-addresses)                                                                |     tcp:443          |     Communication with Azure Databricks webapp                                                                |
	|     databricks-log-blob-storage                                      |     Azure Databricks workspace subnets    |     [Region specific Log Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)         |     https:443        |     To store Azure Databricks audit and cluster logs (anonymized / masked) for support and troubleshooting    |
	|     databricks-artifact-blob-storage                                 |     Azure Databricks workspace subnets    |     [Region specific Artifact Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)    |     https:443        |     Stores Databricks Runtime images to be deployed on cluster nodes                                          |
	|     databricks-dbfs                                                  |     Azure Databricks workspace subnets    |     [DBFS Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#dbfs-root-blob-storage-ip-address)                                                                             |     https:443        |     Azure Databricks workspace root storage                                                                   |
	|     databricks-sql-metastore (OPTIONAL – External Hive Metastore)    |     Azure Databricks workspace subnets    |     [Region specific SQL Metastore Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)            |     tcp:3306         |     Stores metadata for databases and child objects in Azure Databricks workspace                             |

## **Recommended Documents**

* [Monitor usage using cluster, pool, and workspace tags](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/usage-detail-tags-azure)
* [Tagged objects and resources](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/usage-detail-tags-azure#tagged-objects-and-resources)
* [Tag propagation](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/usage-detail-tags-azure#tag-propagation)
* [Azure Databricks pricing](https://azure.microsoft.com/pricing/details/databricks/)
* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) covers the features for the Azure Databricks platform
* [Azure Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features for Databricks cluster runtimes or images, including proprietary features and optimizations
* [Upgrade or Downgrade an Azure Databricks Workspace](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/account#--upgrade-or-downgrade-an-azure-databricks-workspace)
