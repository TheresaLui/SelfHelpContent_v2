<properties
    pageTitle="Configure Consistent indexing mode on your Azure Cosmos DB container"
    description="Configure Consistent indexing mode on your Azure Cosmos DB container"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="213974c8-ed9c-459f-9398-7cdaa3c28856_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Configure Consistent indexing mode on your Azure Cosmos DB container
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "213974c8-ed9c-459f-9398-7cdaa3c28856",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbLazyIndexing",
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
  "learnMoreLink": "https://aka.ms/cosmosdb/how-to-manage-indexing-policy",
  "description": "Configure Consistent indexing mode on your Azure Cosmos DB container",
  "longDescription": "We noticed that your Azure Cosmos DB container is configured with the Lazy indexing mode, which may impact the freshness of query results. We recommend switching to Consistent mode.",
  "potentialBenefits": "Improve query result consistency and reliability",
  "actions": [
    {
      "actionId": "e98bcb9c-c554-46c5-81db-03483f8f38b2",
      "description": "Configure consistent indexing mode",
      "actionType": "Document",
      "documentLink": "https://aka.ms/cosmosdb/how-to-manage-indexing-policy"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "c74a0052-a732-453d-99c3-825671956207",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Configure Consistent indexing mode on your collection",
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
