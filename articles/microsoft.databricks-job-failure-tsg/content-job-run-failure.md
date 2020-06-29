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

1. Was the job run successfully before? 

If any changes were made to job metadata with respect to DBR version, init script and library version or addition of new libraries, revert the changes and run the jobs. 
Some libraries don't support backward compatiablity, so version compatiablity should be throughly checked before migrating jobs clusters to higher DBR versions. Try to run the job after uninstalling the library. If a new version is released for the already existing library, it could be possible that new version might be failing due to version conflict with other dependancies. So install the specific version of the library and rerun the job.


2. If the job is scheduled to run on interactive cluster, check the Ganglia metric to ensure cluster was healthy. If there are too many GC event failure and driver unresponsive event, try to use bigger instance and restart the cluster and then reattempt to run the job.

3. Was the spark job created or the job failed in cluster creation stage prematurely? 

If the job failed prematurely at cluster creation stage, please follow the next steps or refer to [Cluster Troubleshooting](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/321275/Common-Solutions).
