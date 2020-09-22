<properties
	pageTitle="Running jobs are stuck and new jobs are in pending state"
	description="Running jobs are stuck and new jobs are in pending state"
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
	articleId="e1a0f496-96f4-4901-95fb-f5eb2d777eb9"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Running jobs are stuck and new jobs are in pending state

<!--issueDescription-->

After checking the stuck job runs and based on provided details, a quick solution would be to clean up the stuck runs by [cancelling runs](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/jobs?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#--runs-cancel) through REST API. Moreover, we can go through Spark UI to troubleshoot slowest Stage/Task to RCA the problem. 


It is important to mention that by design:

1. The number of jobs a workspace can create in an hour is limited to 5000 (includes run now and runs submit). This limit also affects jobs created by the REST API and notebook workflows.
2. A workspace is limited to 150 concurrent (running) job runs
3. A workspace is limited to 1000 active (running and pending) job runs

Exceeding these limits would usually cause issues when trying to run jobs.<br>
<!--/issueDescription-->

