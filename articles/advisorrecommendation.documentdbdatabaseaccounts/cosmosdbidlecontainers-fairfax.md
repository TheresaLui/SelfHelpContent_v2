<properties
    pageTitle="Delete or reduce provisioned throughput of idle containers"
    description="Delete or reduce provisioned throughput of idle containers"
    authors="rnagpal"
    ms.author="rnagpal"
    articleId="a4255ba5-b07e-45ae-99ca-25e6c2079e3c_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Consider taking action on your idle Azure Cosmos DB containers
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a4255ba5-b07e-45ae-99ca-25e6c2079e3c",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://cdbfairfax.kusto.usgovcloudapi.net').database('LiveSite').IdleContainers",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Low",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbIdleContainers",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "cosmosnotifications@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/CosmosDb",
      "service": "Azure Cosmos DB",
      "team": "Supportability"
    },
    "serviceTreeId": "724c33bf-1ab8-4691-adb1-0e61932919c2"
  },
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/how-to-provision-container-throughput",
  "description": "Consider taking action on your idle Azure Cosmos DB containers",
  "longDescription": "We haven't detected any activity over the past 30 days on one or more of your Azure Cosmos DB containers. Consider lowering their throughput, or deleting them if you don't plan on using them.",
  "potentialBenefits": "Optimize Azure spend",
  "displayLabel": "Decrease provisioned throughput or delete your idle Azure Cosmos DB containers",
  "actions": [
    {
      "actionId": "11179b0e-2d3f-467b-b4e2-7578f1057b52",
      "description": "Reduce provisioned throughput or consider deletion",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "DataExplorerBlade",
      "metadata": {
        "resourceId": "{resourceId}",
        "kind": null
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "a233f3e5-78af-411c-b697-8ac542298aac",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "DatabaseAccountTemplateBladeForGlobalDb",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  }
}
---
