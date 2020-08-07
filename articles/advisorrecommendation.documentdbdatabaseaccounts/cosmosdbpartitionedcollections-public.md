<properties
    pageTitle="Configure your Azure Cosmos DB containers with a partition key"
    description="Configure your Azure Cosmos DB containers with a partition key"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="5b5349fb-b298-41e3-b281-982b7986db67_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Configure your Azure Cosmos DB containers with a partition key
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "5b5349fb-b298-41e3-b281-982b7986db67",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbPartitionedCollections",
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
  "learnMoreLink": "https://aka.ms/cosmosdb/choose-partitionkey",
  "description": "Configure your Azure Cosmos DB containers with a partition key",
  "longDescription": "Your Azure Cosmos DB non-partitioned collections are approaching their provisioned storage quota. Please migrate these collections to new collections with a partition key definition so that they can automatically be scaled out by the service.",
  "potentialBenefits": "Scale your containers seamlessly with increase in storage or request rates without running into any limits",
  "actions": [
    {
      "actionId": "89b9f16e-bf15-4247-a5dc-5f58f366459c",
      "description": "Configure containers with a partition key",
      "actionType": "Document",
      "documentLink": "https://aka.ms/cosmosdb/choose-partitionkey"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "2847eab2-874f-45b1-8517-a5e5709ef280",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Configure your Azure Cosmos DB containers with a partition key",
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
