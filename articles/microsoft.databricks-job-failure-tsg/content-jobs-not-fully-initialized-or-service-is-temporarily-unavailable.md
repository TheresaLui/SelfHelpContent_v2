<properties
	pageTitle="Jobs not fully initialized or service is temporarily unavailable"
	description="Jobs not fully initialized or service is temporarily unavailable"
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
	articleId="f59f4496-7d53-4e1f-9adf-9c151dcaaaaa"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Jobs not fully initialized or service is temporarily unavailable

If customer gets exception message similar to:

```
Jobs not fully initialized yet. Please retry later.
The service at /api/2.0/clusters/start is temporarily unavailable.
```

Issue could be due to:

1. Cluster manager service being unavailable. This is expected during weekly shard maintenance. Please refer?to [Databricks Status](https://status.azuredatabricks.net) page?for any maintenace notification.
2. Azure or Databricks service outages. Please refer?to [Azure](https://status.azure.com/en-gb/status?) and/or [Databricks](https://status.azuredatabricks.net) Status pages for insights. 

If the job was submitted during these windows, then it is recommended to set up retries with job timeout .
