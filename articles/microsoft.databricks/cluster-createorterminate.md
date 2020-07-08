<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster creation failure"
	description="Diagnose and resolve issues with Databricks cluster creation failure"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32730914"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="221c98e1-1bd8-4a79-800d-58bc8ce90b6e"
ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster creation failure

Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes.

### **How To**

* [Use Resource Manager template to create Azure Workspace](https://docs.microsoft.com/azure/azure-databricks/quickstart-create-databricks-workspace-resource-manager-template)
* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Please use [User-defined routes](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/udr.html) to solve this problem.
* [Set Automatic termination](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#automatic-termination) 
* You can use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. The single IP address can be used as an additional security layer with other Azure services and applications that allow access based on specific IP addresses: [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
* If clusters are idle for a period of 30 days then they will be automatically deleted. To avoid this, you can pin them which will not allow for the cluster deletion. For more information:

	* [Pin a Cluster](https://docs.azuredatabricks.net/clusters/clusters-manage.html#pin-a-cluster)
	* [Delete a Cluster](https://docs.azuredatabricks.net/clusters/clusters-manage.html#cluster-delete)

* If Databricks cluster is experiencing **'METASTORE_DOWN'** frequently, interrupting processing and requiring a restart, it could be caused by a known issue of BoneCP not attempting to re-establish the broken connection after the issue happens. To workaround this behavior, you can use the new jar *hikari_datanucleus_2.11_0.1.jar* and copy it to */databricks/hive*:

	* Upload the jar *hikari-datanucleus.jar* to DBFS
	* Go to workspace, create Library, upload the file, and copy the path
	* Create init script using notebook:
 
```
%python

dbutils.fs.put("dbfs:/databricks/init_hikari/<clustername>/hikari.sh","""
   
    	#!/bin/bash
    	cp /dbfs/FileStore/jars/03390a65_418b_49d2_842e_a1069475b3d1-hikari_datanucleus_2_11_0_1-6bb4f.jar /databricks/hive
    	cp /databricks/jars/spark--maven-trees--spark_2.4--com.zaxxer--HikariCP--com.zaxxer__HikariCP__3.1.0.jar /databricks/hive
    
    	""",True)
```
    
	* Edit the cluster and add `spark.hadoop.datanucleus.connectionPoolingType hikari` below Spark configuration under Advanced Options
	* Set up the init script in cluster, confirm changes, and launch the cluster
	
### **Troubleshooting**

* [Unexpected Cluster Termination](https://docs.microsoft.com/azure/databricks/kb/clusters/termination-reasons)
* [Cluster Failed to Launch](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch)
* [Error: The subscription is not registered to use namespace 'Microsoft.Compute'](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-register-provider-errors)

## **Recommended Steps**

* For additional cluster related logs, you can enable [Diagnostics Logging](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/azure-diagnostic-logs)
* If you are getting [error for resource quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors) you can increase quota by following these steps:

    * Go to [subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
    * Select the subscription that needs an increased quota
    * Select Usage + quotas
    * In the upper right corner, select Request increase
    * Fill in the forms for the type of quota you need to increase

Note: To check current resources, please navigate to: Azure Portal under your subscription --> Usage + quotas

> **Known Issue**: Starting 19 Mar 2020 some Azure Databricks customers have encountered error "Azure error code: AllocationFailed" when performing service management operations - such as create, update, scale clusters or submit jobs. We are aware of this issue and are actively working to ensure availability of resources in the quickest time frame possible. We recommend you consider one of the below workarounds:
>
> * Shift the workload towards the end of the working day if possible
> * Try to provision an alternate family VM
> * Increase the size of the VM but provision fewer executors
> * Provision smaller clusters, this increases the chance that enough VMs will be available for your clusters
> * Use pools to reserve instances and configure clusters to use these pools. Please be aware this may increase costs and it’s best if you use this only for essential workloads, if applicable.
> * Deploy the workspace in a different region
>
> If the above workarounds are not viable or did not resolve the issue, please continue with support request creation.
>
> Please visit [blog](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/) for more details on our commitment to customers and Microsoft cloud services continuity.

