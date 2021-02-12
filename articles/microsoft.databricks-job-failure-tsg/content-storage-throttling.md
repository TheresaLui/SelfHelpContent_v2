<properties
	pageTitle="Storage throttling"
	description="Storage throttling"
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
	articleId="677d34ba-bbb1-4704-86cc-de21849c8529"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Storage throttling

Heavy users of Azure Databricks run into storage throttling limits on WASB/ADLS. Databricks hosts worker artifacts (JARs for worker services such as Node Daemon, Log Daemon, etc.) and Spark container images on Azure Blob Store. During high usage (hourly boundaries), requests to pull worker artifacts or Spark containers frequently timeout or become throttled.

User facing error : 

```
Files and folders are being created at too high a rate.
```

### Troubleshooting and Solution

This is storage side limitation as the error suggests, please get azure storage team involved. 

Resolution would be to:

1. Increase the limit for subscription at storage level.
2. Narrow down to specific jobs which are triggering the problem. Look to optimize Spark code to create lesser filed and hence not hit limit of file creation.

If issue persists after trying the suggested approach, please discuss issue further with your SME/TA/EEE using [Ava](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312127/Ava), [file an IcM](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/333941/Escalate-to-Product-Group-team) to get limits increased, and [involve Databricks](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312121/Engaging-Databricks-Support) under spark to get help on optimizing code.
