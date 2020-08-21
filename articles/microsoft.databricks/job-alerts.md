<properties
	pageTitle="Diagnose and resolve issues with Job alerts"
	description="Diagnose and resolve issues with Job alerts"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677701"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="5ca6220e-e35c-4150-b8a3-7f9df4a2a626"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Job alerts

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Problem: Maximum Execution Context or Notebook Attachment Limit Reached](https://docs.microsoft.com/azure/databricks/kb/execution/maximum-execution-context#problem)

> **Known Issue**: Starting 17 June 2020 some Azure Databricks customers in UAE North have encountered error "Azure error code: AllocationFailed" when performing service management operations - such as create, update, scale clusters or submit jobs. We are aware of this issue and are actively working to ensure availability of resources in the quickest time frame possible. We recommend you consider one of the below workarounds:
>
> * Shift the workload towards the end of the working day if possible.
> * Try to provision an alternate family VM
> * Increase the size of the VM but provision fewer executors
> * Provision smaller clusters, this increases the chance that enough VMs will be available for your clusters
> * Use pools to reserve instances and configure clusters to use these pools. Please be aware this may increase costs and it’s best if you use this only for essential workloads, if applicable.
> * Deploy the workspace in a different region
>
> If the above workarounds are not viable or did not resolve the issue, please continue with support request creation
>
> Please visit [blog](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/) for more details on our commitment to customers and Microsoft cloud services continuity.

