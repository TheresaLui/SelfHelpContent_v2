<properties
	pageTitle="Job run failure"
	description="Job run failure"
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
	articleId="c391ec48-011f-41fd-84f1-1aeb10637bc5"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Job run failure

At this point, we need to check the following:

### Was the job run successfully before?

If any changes were made to job metadata with respect to DBR version, init script and library version or addition of new libraries, revert the changes and run the jobs.
Some libraries don't support backward compatibility, so version compatibility should be thoroughly checked before migrating jobs clusters to higher DBR versions. Try to run the job after uninstalling the library. If a new version is released for the already existing library, it could be possible that new version might be failing due to version conflict with other dependencies. So install the specific version of the library and rerun the job.


### Is the job scheduled to run on interactive cluster?

If the job is scheduled to run on interactive cluster, check the [Ganglia metrics](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#ganglia-metrics) to ensure cluster was healthy. If there are too many GC event failures and driver unresponsive events, try to use bigger instance and restart the cluster and then attempt to run the job again.

### Was the spark job created or the job failed in cluster creation stage prematurely?

If the job failed prematurely at cluster creation stage, please follow the next steps or refer to [Cluster Troubleshooting](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/321275/Common-Solutions).
