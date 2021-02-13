<properties 
    pageTitle="Diagnose and resolve issues with Workspace Deployment" 
    description="Diagnose and resolve issues with Workspace Deployment" 
    service="microsoft.databricks" 
    resource="workspaces" 
    authors="lahaddad" 
    ms.author="lahaddad" 
    displayOrder="15" 
    selfHelpType="generic" 
    supportTopicIds="32784353" 
    resourceTags="" 
    productPesIds="16432" 
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="0602cf12-ce6c-48eb-833a-6277f5e46b26" 
    ownershipId="AzureData_AzureDatabricks" 
/> 

# Diagnose and resolve issues with Workspace Deployment 

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes. 

## **Recommended Steps** 

* In April 2020, Azure Databricks added **a new unique per-workspace URL for each workspace**. This per-workspace URL has the following format: `adb-<workspace-id>.<random-number>.azuredatabricks.net`. This per-workspace URL is complementary to the existing regional URLs (<region>.azuredatabricks.net) that you have used up until now to access your workspaces. Both URLs continue to be supported. However, because Azure Databricks adds more infrastructure into existing regions, the regional URLs for new workspaces may vary from those of your existing workspaces. Therefore, **we strongly recommend that you use the new per-workspace URL in scripts or other automation that you want to use with multiple workspaces**. Follow the instructions in the links below: 

  

    * [How do I launch my workspace using the per-workspace URL?](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#launch-a-workspace-using-the-per-workspace-url) 

    * [Migrate scripts and other automation](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#migrate-your-scripts-to-use-per-workspace-urls) 

    * [Find the regional URL for a workspace](https://docs.microsoft.com/azure/databricks/workspace/per-workspace-urls#find-the-legacy-regional-url-for-a-workspace) 

* When using Azure Databricks, you'll find that Azure automatically creates a **Databricks workspace**, as well as a **managed resource group (databricks-rg-xxx-xxx)** containing all the resources needed to run the cluster. This is why a workspace and a managed resource group suddenly appear.

  This managed resource group (MRG) is protected by a system-level lock to prevent deletions and modifications. The only way to directly remove the lock is to delete the service. However, by making changes to the parent resource group, those changes will be correspondingly updated in the managed resource group. 

   * Learn about [managed applications and locks](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources#managed-applications-and-locks) 


* Deploying workspace through ARM Templates will fail if you use existing resource group name as a managed resource group. Ensure that the [Managed Resource group](https://docs.microsoft.com/azure/managed-applications/overview#managed-resource-group) in the ARM template doesn't already exist within the subscription. 

* Avoid having any special characters as the first or last character in a workspace name. The maximum length for a Managed Resource group name is 90 characters. **Invalid characters will cause the workspace creation to fail**.   

* Deploying Azure Databricks data plane resources to your own VNet lets you take advantage of flexible CIDR ranges. If your **current workspace cannot accommodate the required number of active cluster nodes**: 

    * You cannot replace the VNet for an existing workspace 
    * You cannot change subnet CIDR range for an existing workspace 

    Instead, we recommend that you create another workspace in a larger VNet. Follow these [detailed migration steps](https://docs.microsoft.com/azure/azure-databricks/howto-regional-disaster-recovery#detailed-migration-steps) to copy resources (notebooks, cluster configurations, jobs) from the old workspace to the new one. 

 

* **Implement workload through Azure Firewall to Azure Databricks.** Note the Databricks control plane endpoints for your workspace (map them based on the region of your workspace) when configuring Azure Firewall rules: 

  |     Name                                                             |     Source                                |     Destination                                                                                                                                                                                                                                 |     Protocol:Port    |     Purpose                                                                                                   | 
  |----------------------------------------------------------------------|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|---------------------------------------------------------------------------------------------------------------|
  |     databricks-webapp                                                |     Azure Databricks workspace subnets    |     [Region specific Webapp Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#control-plane-nat-and-webapp-ip-addresses)                                                                |     tcp:443          |     Communication with Azure Databricks webapp|
  |     databricks-log-blob-storage                                      |     Azure Databricks workspace subnets    |     [Region specific Log Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)         |     https:443        |     To store Azure Databricks audit and cluster logs (anonymized / masked) for support and troubleshooting    |
    |     databricks-artifact-blob-storage                                 |     Azure Databricks workspace subnets    |     [Region specific Artifact Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)    |     https:443        |     Stores Databricks Runtime images to be deployed on cluster nodes                                          |
    |     databricks-dbfs                                                  |     Azure Databricks workspace subnets    |     [DBFS Blob Storage Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#dbfs-root-blob-storage-ip-address)                                                                             |     https:443        |     Azure Databricks workspace root storage                                                                   |
    |     databricks-sql-metastore (OPTIONAL – External Hive Metastore)    |     Azure Databricks workspace subnets    |     [Region specific SQL Metastore Endpoint](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/udr#--metastore-artifact-blob-storage-log-blob-storage-and-event-hub-endpoint-ip-addresses)            |     tcp:3306         |     Stores metadata for databases and child objects in Azure Databricks workspace                             | 

 

* Learn [how to assign a single public IP for VNet-injected workspaces using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip) 

 

## **Recommended Documents**  

* [Azure Databricks pricing](https://azure.microsoft.com/pricing/details/databricks/) 

* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) covers the features for the Azure Databricks platform 

* [Azure Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features for Databricks cluster runtimes or images, including proprietary features and optimizations 

* [Upgrade or Downgrade an Azure Databricks Workspace](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/account#--upgrade-or-downgrade-an-azure-databricks-workspace) 
