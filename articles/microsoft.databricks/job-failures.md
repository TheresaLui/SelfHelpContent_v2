<properties
	pageTitle="Diagnose and resolve job failures"
	description="Diagnose and resolve job failures"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677702"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
	articleId="f951a9e3-02de-4747-8f14-e7c8fc1537ae"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve job failures

## **Recommended Steps**

### **Troubleshooting**

* [Cluster Timeout](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#cluster-timeout) for Error Messages:
````
Driver failed to start in time
INTERNAL_ERROR: The Spark driver failed to start within 300 seconds; Cluster failed to be healthy within 200 seconds
````
* [Global or cluster-specific init scripts](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#global-or-cluster-specific-init-scripts) for Error Message: 
````
The cluster could not be started in 50 minutes. Cause: Timed out with exception after <xxx> attempts)
````
* [Too many libraries installed in cluster UI](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#too-many-libraries-installed-in-cluster-ui) for Error Message: 
````
Library installation timed out after 1800 seconds. Libraries that are not yet installed:
````
* [Cloud provider limit](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#cloud-provider-limit) for Error: 
````
Cluster terminated. Reason: Cloud Provider Limit
````
* [Cloud provider shutdown](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#cloud-provider-shutdown) for Error:
````Cluster terminated. Reason: Cloud Provider Shutdown
````
* [Instances unreachable](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable) for Error Messages: 
````
Cluster terminated. Reason: Instances Unreachable 
An unexpected error was encountered while setting up the cluster.)
````

## **Recommended Documents**

* [Problem: Spark Job Fails with Driver is temporarily unavailable](https://kb.azuredatabricks.net/jobs/driver-unavailable.html)
* [Problem: Job Fails Due to Job Rate Limit](https://kb.azuredatabricks.net/jobs/job-rate-limit.html)
* [Problem: Azure Databricks Job Fails Because Library is Not Installed](https://kb.azuredatabricks.net/jobs/job-fails-no-library.html)
* [Problem: Maximum Execution Context or Notebook Attachment Limit Reached](https://kb.azuredatabricks.net/execution/maximum-execution-context.html)
