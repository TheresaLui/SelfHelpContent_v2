<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster creation, termination, or sizing"
	description="Diagnose and resolve issues with Databricks cluster creation, termination, or sizing"
	service="microsoft.databricks"
	resource="workspaces"
	authors="mspreshah"
	ms.author="preshah"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32612187"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="4e43f6fa-57dd-4bd3-b6f4-9b10f7a8dccc"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster creation, termination, or sizing

## **Recommended Steps**

Below are details on how to setup, terminate and change the size of a Azure Databricks cluster.  

* You can create and manage clusters using the [UI](https://docs.azuredatabricks.net/user-guide/clusters/create.html), [Databricks CLI](https://docs.azuredatabricks.net/user-guide/dev-tools/databricks-cli.html#databricks-cli), and by invoking the [clusters API](https://docs.azuredatabricks.net/api/latest/clusters.html#cluster-api)
* The [size of the cluster](https://docs.azuredatabricks.net/user-guide/clusters/sizing.html) is initially set when the cluster is created. You can either provide a fixed number of workers for the cluster or provide a minimum and maximum number of workers for the cluster to enable autoscaling. You can change the size of the cluster after it is created by editing the cluster configuration.  
* You can manually [terminate a cluster](https://docs.azuredatabricks.net/user-guide/clusters/terminate.html), or configure the cluster to automatically terminate after a specified period of inactivity
* When you terminate a cluster, the terminated cluster cannot run notebooks or jobs, but its configuration is stored so that it can be reused at a later point in time

## **Recommended Documents**

* [Autoscaling of clusters](https://docs.azuredatabricks.net/user-guide/clusters/sizing.html)
* [Optimized autoscaling](https://databricks.com/blog/2018/05/02/introducing-databricks-optimized-auto-scaling.html)
