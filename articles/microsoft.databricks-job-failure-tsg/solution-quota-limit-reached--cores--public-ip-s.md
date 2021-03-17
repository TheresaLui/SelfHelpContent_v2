<properties
	pageTitle="Quota limit reached (cores, public IP?s,...)"
	description="Quota limit reached (cores, public IP?s,...)"
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
	articleId="1a06626d-0789-406e-ac1b-4e92562f5a92"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Quota limit reached (cores, public IPs,...)

<!--issueDescription-->

We have accessed your workspace and cluster event logs, and it seems that cluster launch is failing due to Databricks not being able to acquire VMs getting this error:

```
please paste the error here
```

To resolve the issue:

1. You can either **stop unused clusters** to release resources
2. Or if the first suggested solution is not feasible, please **open a case with Azure Subscription Management team** making sure to incluse these details: 
   Subscription ID, Region, VM type, Current available number of cores, Number of cores to be added

<!--/issueDescription-->

## **Recommended Documents**
* [Step by step on opening the case](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests)
* [Check resource usage against limits](https://docs.microsoft.com/azure/networking/check-usage-against-limits)
