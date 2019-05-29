<properties
    pageTitle="Provision the optimal amount of Request Units for Azure Cosmos DB"
    description="Provision the optimal amount of Request Units for Azure Cosmos DB"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="8b993855-1b3f-4392-8860-6ed4f5afd8a7_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Provision the optimal amount of Request Units for Azure Cosmos DB
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "8b993855-1b3f-4392-8860-6ed4f5afd8a7",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "Microsoft.Cloud.AzureCosmosDBRecommendationsTableProd",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Low",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBOptimizeRU",
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
  "learnMoreLink": "https://aka.ms/aa_cosmosdb_ru_learnmore",
  "description": "Provision the optimal amount of Request Units for Azure Cosmos DB",
  "longDescription": "This recommendation analyzes usage data in the past 3 weeks and recommends the optimal amount of Request Units to provision for an Azure Cosmos DB. The recommendation is based on the maximum Request Units used in every 5-minute interval and any throttling reports in the 3-week period.",
  "potentialBenefits": "Optimize Azure spend",
  "actions": [
    {
      "actionId": "9fbbd199-bc20-4c40-812b-1030583b464f",
      "description": "Adjust your provisioned RUs to the optimal number",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aa_cosmosdb_ru_action"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "2fad54ad-2907-4a6a-b5c2-180c726fa3e4",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "DatabaseAccountTemplateBladeForGlobalDb",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Optimize RU provisioning for Azure Cosmos DB",
  "additionalColumns": [
    {
      "name": "DatabaseName",
      "title": "Database Name"
    },
    {
      "name": "CollectionName",
      "title": "Collection Name"
    },
    {
      "name": "RecommendedThroughput",
      "title": "Recommended Throughput"
    }
  ],
  "costSavingInfo": "*You can save up to the stated amount if you adjust the provisioned Request Units to the recommended amount for each collection."
}
---
