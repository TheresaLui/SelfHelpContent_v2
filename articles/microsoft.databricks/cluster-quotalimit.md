<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster creation due to quota limit"
	description="Diagnose and resolve issues with Databricks cluster creation due to quota limit"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677680"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="bc33791c-7c27-461b-b0d0-989c567e50a7"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster creation due to quota limit

## **Recommended Steps**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes

* To expedite the process to increase quota, please follow the steps:

    * Go to [subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
    * Select the subscription whose quota you want to increase
    * Select Usage + quotas
    * In the upper right corner, select Request increase
    * Fill in the forms for the type of quota you need to increase
  
	For detailed instructions please follow the article [here](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests#request-a-standard-quota-increase-from-subscriptions).

* To check current resources, please navigate to: Azure Portal under your subscription --> Usage + quotas

## **Recommended Documents**

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
