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

Based on the provided details, issue is most likely due to:<br>
<br>
1. Cluster manager service being unavailable. This is expected during weekly shard maintenance. Please refer to [Databricks Status](https://status.azuredatabricks.net) page for any maintenance notification.<br>
2. Azure or Databricks service outages. Please refer to [Azure Status](https://status.azure.com/status?) and [Databricks Status](https://status.azuredatabricks.net) pages for insights. <br>
<br>

If the job was submitted during these windows, then it is recommended to set up retries with job timeout. Please check this [document](https://docs.microsoft.com/azure/databricks/jobs?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#advanced-job-options) for more details.

Please check it and let us know if issue persist or any concern, so we assist further accordingly.

<!--/issueDescription-->

