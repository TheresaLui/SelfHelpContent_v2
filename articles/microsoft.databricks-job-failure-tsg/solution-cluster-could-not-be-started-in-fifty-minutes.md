<properties
	pageTitle="Cluster could not be started in 50 minutes"
	description="Cluster could not be started in 50 minutes"
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
	articleId="cd047075-4a83-489e-92f8-b14c9250204e"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Cluster could not be started in 50 minutes

<!--issueDescription-->

After checking the job runs and based on provided details, job is failing due Cluster startup failure. This error happens when execution of initscript gets hung and cluster creation gets timed out. Please go through the following steps to resolve the issue:

1. Check for any global initscripts under *dbfs:/databricks/init/* or cluster scoped initscripts *%sh /dbfs/databricks/init/<ClusterName>* 
2. Remove the initscript and try to create the cluster to confirm the issue with initscript
3. If this is cluster scoped initscript, create a test cluster without any init script and run the each command in initscript manually to find which command is getting hung and try to fix it
4. Convert scripts to cluster scoped init scripts

<!--/issueDescription-->

## **Recommended Documents**

* [Cluster node initialization scripts](https://docs.microsoft.com/azure/databricks/clusters/init-scripts)
