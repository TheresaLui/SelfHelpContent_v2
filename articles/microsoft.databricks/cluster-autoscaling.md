<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster auto scaling"
	description="Diagnose and resolve issues with Databricks cluster auto scaling"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677670"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="f1a01f3b-d175-4387-8b3b-d09082cbe570"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster auto scaling

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Enable and configure autoscaling](https://docs.databricks.com/user-guide/clusters/sizing.html#enable-and-configure-autoscaling)
* [How autoscaling behaves](https://docs.databricks.com/user-guide/clusters/sizing.html#how-autoscaling-behaves)
* [Introducing Databricks Optimized Autoscaling on Apache Spark](https://databricks.com/blog/2018/05/02/introducing-databricks-optimized-auto-scaling.html)

> **Known Issue**: Starting 19 Mar 2020 some Azure Databricks customers have encountered error "Azure error code: AllocationFailed" when performing service management operations, such as create, update, scale clusters or submit jobs. We are aware of this issue and are actively working to ensure availability of resources in the quickest time frame possible. We recommend you consider one of the below workarounds:
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

