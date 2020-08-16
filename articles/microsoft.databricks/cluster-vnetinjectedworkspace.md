<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster creation in a VNET injected workspace"
	description="Diagnose and resolve issues with Databricks cluster creation in a VNET injected workspace"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677681"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a87a5e09-90f1-4c5d-a77b-5ea9a3436bc9"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster creation in a VNET injected workspace

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [How to: Upgrade your VNet Injection Preview Workspace to GA](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject-upgrade)
* You can use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. The single IP address can be used as an additional security layer with other Azure services and applications that allow access based on specific IP addresses: [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
* [Virtual Network Peering](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/vnet-peering.html)
* [Instances unreachable](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable)
* [Configure custom DNS](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--option-configure-custom-dns)

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
