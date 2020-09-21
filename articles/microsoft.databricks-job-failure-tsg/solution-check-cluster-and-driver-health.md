<properties
	pageTitle="Check cluster and driver health"
	description="Check cluster and driver health"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ea613e7a-4361-47ca-9108-1c76436a3e84"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check cluster and driver health

<!--issueDescription-->

Based on provided details and our investigation, since the job is scheduled to run on interactive cluster, we need to check the Ganglia metrics to ensure cluster was healthy at issue time. If there are too many GC event failure and driver unresponsive event, please follow these steps:
1. Try to use bigger instance
2. Restart the cluster
3. Reattempt to run the job

<!--/issueDescription-->

## Recommended Documents

* [Ganglia metrics](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#ganglia-metrics)
* [View cluster logs](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#--view-cluster-logs)
* [Restart clusters](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#--start-a-cluster)
