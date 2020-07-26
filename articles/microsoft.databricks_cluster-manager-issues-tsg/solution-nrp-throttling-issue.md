<properties
	pageTitle="NRP Throttling Issue"
	description="NRP Throttling Issue"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="26735410-2f4e-4903-a543-931e2049488f"
   	ownershipId="AzureData_AzureDatabricks"
/>

# NRP Throttling Issue

<!--issueDescription-->

After troubleshooting the issue, it seems cluster is failing at creation stage due to NRP throttling. This usually occurs when there is about 50 simultaneous write operations (create/delete) on public IPs in a given subscription which creates a slowdown on NRP operations and induces throttling, and results in all the requests above the limit failures. 

Recommended solution to this problem would be to use Pools to reduce churn of resources.

Another suggested workaround is to perform resizing and/or create clusters in smaller batches (around 50 workers max at one time). This number can also be affected by whatever else is occurring in the subscription since the throttling is occurring at the subscription level (whether databricks or non-databricks related Azure events).

## Recommended Documents
* [Pools](https://docs.microsoft.com/azure/databricks/clusters/instance-pools/)
* [Azure Requests Limits and Throttling](https://docs.microsoft.com/azure/azure-resource-manager/management/request-limits-and-throttling)

Please try the suggested workaround(s) and let us know if the issue persists or if any concerns.

<!--/issueDescription-->
