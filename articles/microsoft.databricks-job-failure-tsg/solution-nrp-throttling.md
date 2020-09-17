<properties
	pageTitle="NRP throttling"
	description="NRP throttling"
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
	articleId="0009906a-33cd-4094-bc80-a103393ee1f1"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# NRP throttling

<!--issueDescription-->

After troubleshooting the issue, it seems jobs are failing at cluster creation stage due to NRP throttling. This usually occurs when there is about 50 simultaneous write operations (create/delete) on public IPs in a given subscription which creates a slowdown on NRP operations and induces throttling, and results in all the requests above the limit failures.

User facing Error:

```
Subscription XXX was used to perform too many calls within last 5 minutes. The number of calls exceeds Microsoft. Network throttling limit. or Encountered Azure Resource provider throttling. Please try again later.
```
Recommended solution to this problem would be to use Pools to reduce churn of resources.

Another suggested workaround is to perform resizing and/or create clusters in smaller batches (around 50 workers max at one time). This number can also be affected by whatever else is occurring in the subscription since the throttling is occurring at the subscription level (whether databricks or non-databricks related Azure events).<br>

<!--/issueDescription-->

### Recommended Documents
* [Pools](https://docs.microsoft.com/azure/databricks/clusters/instance-pools/)
* [Azure Requests Limits and Throttling](https://docs.microsoft.com/azure/azure-resource-manager/management/request-limits-and-throttling)
