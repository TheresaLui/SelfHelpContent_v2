<properties
	pageTitle="Check if there are any existing In Progress run which is getting delayed in completion or stuck"
	description="Check if there are any existing In Progress run which is getting delayed in completion or stuck"
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
	articleId="53c73371-eccd-4461-9af4-7a80b1f666ca"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if there are any existing In Progress run which is getting delayed in completion or stuck

You can run the following command in Kusto to check if the pipeline run is in InProgress state or getting delayed/stuck in completion.

```
cluster('adfcus').database('AzureDataFactory').PipelineRuns | union cluster('adfneu').database('AzureDataFactory').PipelineRuns
| where TIMESTAMP >= ago(7d)
| where pipelineName == "<PipelineName>"
| where dataFactoryName == "<DataFactoryName>"
| where status == "InProgress"
| project PreciseTimeStamp, subscriptionId, dataFactoryName, runId, pipelineName , location, status, failureType, start, end, predecessors
| order by PreciseTimeStamp desc
```
