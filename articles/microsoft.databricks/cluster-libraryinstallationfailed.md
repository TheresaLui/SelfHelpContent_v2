<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster creation failure due to failed library installation"
	description="Diagnose and resolve issues with Databricks cluster creation failure due to failed library installation"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677679"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
	articleId="b508ffff-e283-4073-ad31-0d3aeff428bd"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster creation failure due to failed library installation

**Known Issue**: Starting 19 Mar 2020 if you encountered error "Azure error code: AllocationFailed" when performing service management operations - such as create, update, scale clusters or submit jobs. We are aware of this issue and are actively working to ensure availability of resources in the quickest time frame possible. We recommend you consider one of the below workarounds:

* Shift the workload towards the end of the working day if possible.
* Try to provision an alternate family VM
* Increase the size of the VM but provision fewer executors
* Provision smaller clusters, this increases the chance that enough VMs will be available for your clusters
* Use pools to reserve instances and configure clusters to use these pools. Please be aware this may increase costs and it’s best if you use this only for essential workloads, if applicable.
* Deploy the workspace in a different region

If the above workarounds are not viable or did not resolve the issue, please continue with support request creation

Please visit [blog](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/) for more details on our commitment to customers and Microsoft cloud services continuity.


## **Recommended Documents**

* [Library Unavailability Causing Job Failures](https://kb.azuredatabricks.net/libraries/library-install-latency.html#problem-library-unavailability-causing-job-failures)
* [Cluster Cancels Python Command Execution due to Library Conflict](https://kb.azuredatabricks.net/python/python-command-cancelled.html#problem-cluster-cancels-python-command-execution-due-to-library-conflict)
