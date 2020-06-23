<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster creation due to core quota limit"
	description="Diagnose and resolve issues with Databricks cluster creation due to core quota limit"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677649"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1426739b-ba80-4f23-a292-0ef08ed3c42e"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster creation due to quota limit

## **Recommended Steps**

* To submit an expedited request for core quota limit increase follow the [steps here](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests) 
* To check current resources, navigate to: Azure Portal under your subscription --> Usage + quotas

## **Recommended Documents**

* For current status of Azure Databricks Service by region and to subscribe for updates on status changes, browse to [Azure Databricks Status Page](https://status.azuredatabricks.net/)
* [Azure Databricks initiated request limit exceeded](https://kb.azuredatabricks.net/clusters/termination-reasons.html#databricks-initiated-request-limit-exceeded)
* [Launch failure](https://kb.azuredatabricks.net/clusters/termination-reasons.html#launch-failure)



> **Known Issue**: Starting 19 Mar 2020 some Azure Databricks customers have encountered error "Azure error code: AllocationFailed" when performing service management operations - such as create, update, scale clusters or submit jobs. We are aware of this issue and are actively working to ensure availability of resources in the quickest time frame possible. We recommend you consider one of the below workarounds:
>
> * Shift the workload towards the end of the working day if possible
> * Try to provision an alternate family VM
> * Increase the size of the VM but provision fewer executors
> * Provision smaller clusters, this increases the chance that enough VMs will be available for your clusters
> * Use pools to reserve instances and configure clusters to use these pools. Please be aware this may increase costs and it’s best if you use this only for essential workloads, if applicable.
> * Deploy the workspace in a different region
>
> If the above workarounds are not viable or did not resolve the issue, please continue with support request creation.
>
> Please visit [blog](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/) for more details on our commitment to customers and Microsoft cloud services continuity.
