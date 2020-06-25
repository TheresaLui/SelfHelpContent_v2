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

Check the running job runs if they are long running and exceeding the expected run time and if they are in hung state. If so, all future job runs will be in pending state. To find number of jobs, you can use [Jobs REST API](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/jobs?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#--runs-list) or CLI as below:

*databricks runs list  --limit 1000 | egrep -c 'RUNNING|PENDING'*

If customer is looking for cleanup help, you can [cancel runs](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/jobs?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#--runs-cancel) through REST API to clean up hung job runs.

Moreover, use Spark UI to troubleshoot slowest Stage/Task to RCA the problem.
