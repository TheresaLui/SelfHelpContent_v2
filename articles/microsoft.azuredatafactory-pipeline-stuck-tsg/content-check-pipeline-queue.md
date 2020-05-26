<properties
	pageTitle="Check if there are any existing pipeline with status as Queued"
	description="Check if there are any existing pipeline with status as Queued"
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
	articleId="8b6a55bb-fcf7-4ad6-aa19-2ffccf4c7fad"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if there are any existing pipeline with status as Queued?

Run the following Kusto Query to check the status of the Pipeline Runs: 

```
cluster('adfcus').database('AzureDataFactory').PipelineRuns | union cluster('adfneu').database('AzureDataFactory').PipelineRuns
| where TIMESTAMP >= ago(7d)
| where pipelineName == "<PipelineName>"
| where dataFactoryName == "<DataFactoryName>"
| where status == "Queued"
| project PreciseTimeStamp, subscriptionId, dataFactoryName, runId, pipelineName , location, status, failureType, start, end, predecessors
| order by PreciseTimeStamp desc
```
