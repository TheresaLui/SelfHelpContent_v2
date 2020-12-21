<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster auto scaling"
	description="Diagnose and resolve issues with Databricks cluster auto scaling"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677670"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="f1a01f3b-d175-4387-8b3b-d09082cbe570"
	ownershipId="AzureData_AzureDatabricks"
/>
# Diagnose and resolve issues with Databricks cluster auto scaling

## **Recommended Steps**

* Autoscaling is not available for spark-submit jobs
* [Resize a cluster using Clusters API](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/clusters#--resize) to have a desired number of workers. The cluster must be in the `RUNNING` state.

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Cluster size and autoscaling](https://docs.microsoft.com/azure/databricks/clusters/configure#--cluster-size-and-autoscaling)

    * [Autoscaling types](https://docs.microsoft.com/azure/databricks/clusters/configure#autoscaling-types)
    * [How autoscaling behaves](https://docs.microsoft.com/azure/databricks/clusters/configure#how-autoscaling-behaves)
    * [Enable and configure autoscaling](https://docs.microsoft.com/azure/databricks/clusters/configure#enable-and-configure-autoscaling)
  
* [Introducing Databricks Optimized Autoscaling on Apache Spark](https://databricks.com/blog/2018/05/02/introducing-databricks-optimized-auto-scaling.html)
* [Clusters: tips and troubleshooting](https://docs.microsoft.com/azure/databricks/kb/clusters/)
