<properties
	pageTitle="How to check if this run is in status Queued"
	description="How to check if this run is in status Queued"
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
	articleId="1ad4f5d5-36d2-4640-b369-cbd0d570832c"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if this run is in status Queued?

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