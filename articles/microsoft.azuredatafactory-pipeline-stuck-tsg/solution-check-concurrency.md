<properties
	pageTitle="Check concurrency value"
	description="Check concurrency value"
    service="Microsoft.DataFactory"
    resource="Microsoft.DataFactory/register,Microsoft.DataFactory/datafactories,Microsoft.DataFactory/factories"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="da5a4b71-1e32-4c77-b607-41c9b0d7f3cc"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check concurrency value
<!--issueDescription-->
Dear Customer,<br>

We identified an issue with that the pipeline **<PipelineName>** is stuck and have a few runs in the queued state.<br> 

Please check the pipeline concurrency value. If the concurrency is 1, then it may happen that other pipelines are waiting for resources to be released. Try increasing the concurrency value and check.<br>

You may refer to the following articles to check concurrency:<br>
https://docs.microsoft.com/en-us/azure/data-factory/concepts-pipelines-activities#pipeline-json <br>

If the concurrency value is already set to a larger value, then the issue could be caused due to the Tumbling window trigger. <br>

Try setting the concurrency limits for the tumbling window trigger. You may set value between 1 and 50 concurrent triggered pipeline runs.
<!--/issueDescription-->

**Recommended Documents**

1. [Check concurrency](https://docs.microsoft.com/azure/data-factory/concepts-pipelines-activities#pipeline-json)