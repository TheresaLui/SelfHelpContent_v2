<properties
    pageTitle="Configure your Azure Cosmos DB containers with a partition key"
    description="Configure your Azure Cosmos DB containers with a partition key"
    authors="rnagpal"
    ms.author="rnagpal"
    articleId="9d701f42-13e2-4876-9c2c-64c79dbf3651_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Configure your Azure Cosmos DB containers with a partition key
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "acac062f-9b64-4634-9406-04de711c4d5d",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://cdbfairfax.kusto.usgovcloudapi.net').database('LiveSite').FixedCollection",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbPartitionedCollections",
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
  "learnMoreLink": "https://aka.ms/cosmosdb/choose-partitionkey",
  "description": "Configure your Azure Cosmos DB containers with a partition key",
  "longDescription": "Your Azure Cosmos DB non-partitioned collections are approaching their provisioned storage quota. Please migrate these collections to new collections with a partition key definition so that they can automatically be scaled out by the service.",
  "potentialBenefits": "Scale your containers seamlessly with increase in storage or request rates without running into any limits",
  "displayLabel": "Configure your Azure Cosmos DB containers with a partition key",
  "additionalColumns": [
    {
      "name": "DatabaseName",
      "title": "Database"
    },
    {
      "name": "CollectionName",
      "title": "Container"
    }
  ],
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
  }
}
---
