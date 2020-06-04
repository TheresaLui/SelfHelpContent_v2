<properties
    pageTitle="Configure your Azure Cosmos DB query page size (MaxItemCount) to -1"
    description="Configure your Azure Cosmos DB query page size (MaxItemCount) to -1"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="e27c5181-5005-4dc3-a449-89b726a3bf54_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Configure your Azure Cosmos DB query page size (MaxItemCount) to -1
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "e27c5181-5005-4dc3-a449-89b726a3bf54",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbQueryPageSize",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "aadevteam@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Azure Advisor",
      "team": "Azure Advisor"
    },
    "serviceTreeId": "f6d7f416-ee14-4943-894b-1abca9140b74"
  },
  "ingestionClientIdentities": [
    "6c75c76c-7792-4dd0-8e85-ad598f14bc93",
    "db97364d-48bf-4567-af34-e0843d0ee0af",
    "bd26e40e-c0cc-4d1d-8801-569dac0cd7fe"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/cosmosdb/sql-api-query-metrics-max-item-count",
  "description": "Configure your Azure Cosmos DB query page size (MaxItemCount) to -1",
  "longDescription": "You are using the query page size of 100 for queries for your Azure Cosmos DB container. We recommend using a page size of -1 for faster scans.",
  "potentialBenefits": "End to end query latency will be improved significantly",
  "actions": [
    {
      "actionId": "29039a89-7db5-44c6-b8f9-cc2cc021e93d",
      "description": "Use a page size of -1",
      "actionType": "Document",
      "documentLink": "https://aka.ms/cosmosdb/sql-api-query-metrics-max-item-count"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "f0a1b121-2642-4c0a-91aa-6ca4e5e5463b",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Configure your Azure Cosmos DB query page size (MaxItemCount) to -1",
  "additionalColumns": [
    {
      "name": "databaseName",
      "title": "Database"
    },
    {
      "name": "containerName",
      "title": "Container"
    }
  ]
}
---
