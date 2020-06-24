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
	articleId="f59f4496-7d53-4e1f-9adf-9c151dc2322f"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Jobs not fully initialized or service is temporarily unavailable

<!--issueDescription-->

Based on the provided details, issue could be due to:<br>
<br>
1. Cluster manager service being unavailable. This is expected during weekly shard maintenance. Please refer?to [Databricks Status](https://status.azuredatabricks.net) page?for any maintenace notification.<br>
2. Azure or Databricks service outages. Please refer?to [Azure](https://status.azure.com/en-gb/status?) and/or [Databricks](https://status.azuredatabricks.net) Status pages for insights. <br>
<br>
<br>
If the job was submitted during these windows, then it is recommended to set up retries with job timeout. Please check this [document](https://docs.microsoft.com/en-us/azure/databricks/jobs?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#advanced-job-options) for more details.<br>

<!--/issueDescription-->

