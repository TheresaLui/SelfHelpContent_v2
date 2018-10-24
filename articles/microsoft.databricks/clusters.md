<properties
	pageTitle="Databricks cluster creation, terminating or sizing issues"
	description="Databricks cluster creation, terminating or sizing issues"
	service="microsoft.Databricks"
	resource="clusters"
	authors="mspreshah"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds="32612187"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
/>

# Azure Databricks cluster creation, termination and sizing

## **Recommended steps**

The folllowing details explain how to setup Azure Databricks clusters, termination clusters and sizing.

(1) You can create and manage clusters using the UI, CLI and by invoking the clusters API
(2) When you terminate a cluster, the terminated cluster cannot run notebooks or jobs, but its configuration is stored so that it can be reused at a later point in time
(3) You can manually terminate a cluster or configure the cluster to automatically terminate after a specified period of inactivity
(4) When you create a cluster, you can either provide a fixed number of workers for the cluster or provide a minimum and maximum number of workers for the cluster to enable autoscaling

## **Recommended documents**
1. [Clusters on Azure Databricks](https://docs.azuredatabricks.net/user-guide/clusters/index.html)
2. [Autoscaling of clusters](https://docs.azuredatabricks.net/user-guide/clusters/sizing.html)
3. [Optimized autoscaling](https://databricks.com/blog/2018/05/02/introducing-databricks-optimized-auto-scaling.html)
