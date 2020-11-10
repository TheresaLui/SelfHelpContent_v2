<properties
    pageTitle="Provision the optimal amount of Request Units for Azure Cosmos DB"
    description="Provision the optimal amount of Request Units for Azure Cosmos DB"
    authors="raldaba"
    ms.author="aoaft"
    articleId="8b993855-1b3f-4392-8860-6ed4f5afd8a7_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureData_AzureCosmosDB"
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
    "streamNamespace": "cluster('https://cerebro.centralus.kusto.windows.net').database('Publish').GetAcdbThroughputAzureAdvisorRecs",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Low",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBOptimizeRU",
  "recommendationMetadataState": "Active",
  "recommendationScope": "Internal",
  "portalFeatures": [],
  "owner": {
    "email": "aoaft@microsoft.com",
    "icm": {
      "routingId": "AROTOOLBOX\\AROToolboxDevTeam",
      "service": "Azure Optimization Automation",
      "team": "Azure Optimization Automation"
    },
    "serviceTreeId": "a3db6cf3-640c-4340-8381-108d31853b7f"
  },
  "ingestionClientIdentities": [
    "6c75c76c-7792-4dd0-8e85-ad598f14bc93",
    "db97364d-48bf-4567-af34-e0843d0ee0af",
    "bd26e40e-c0cc-4d1d-8801-569dac0cd7fe",
    "9c14bff5-1bda-4de6-a74f-4c3caa370570"
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
