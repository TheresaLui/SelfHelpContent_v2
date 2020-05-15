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
	cloudEnvironments="public, fairfax, usnat, ussec"
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

* [Global or cluster-specific init scripts](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#global-or-

cluster-specific-init-scripts) for Error Message: 
````
The cluster could not be started in 50 minutes. Cause: Timed out with exception after <xxx> attempts
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

```
Cluster terminated. Reason: Cloud Provider Shutdown
```

* [Instances unreachable](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable) for Error Messages: 

````
Cluster terminated. Reason: Instances Unreachable 
An unexpected error was encountered while setting up the cluster.
````

## **Recommended Documents**

* [Problem: Spark Job Fails with Driver is temporarily unavailable](https://kb.azuredatabricks.net/jobs/driver-unavailable.html)
* [Problem: Job Fails Due to Job Rate Limit](https://kb.azuredatabricks.net/jobs/job-rate-limit.html)
* [Problem: Azure Databricks Job Fails Because Library is Not Installed](https://kb.azuredatabricks.net/jobs/job-fails-no-library.html)
* [Problem: Maximum Execution Context or Notebook Attachment Limit Reached](https://kb.azuredatabricks.net/execution/maximum-execution-context.html)

> **Known Issue**: Starting 19 Mar 2020 some Azure Databricks customers have encountered error "Azure error code: AllocationFailed" when performing service management operations - such as create, update, scale clusters or submit jobs. We are aware of this issue and are actively working to ensure availability of resources in the quickest time frame possible. We recommend you consider one of the below workarounds:
>
> * Shift the workload towards the end of the working day if possible
> * Try to provision an alternate family VM
> * Increase the size of the VM but provision fewer executors
> * Provision smaller clusters, this increases the chance that enough VMs will be available for your clusters
> * Use pools to reserve instances and configure clusters to use these pools. Please be aware this may increase costs and it’s best if you use this only for essential workloads, if applicable.
> * Deploy the workspace in a different region
>
> If the above workarounds are not viable or did not resolve the issue, please continue with support request creation
>
> Please visit [blog](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/) for more details on our commitment to customers and Microsoft cloud services continuity.
