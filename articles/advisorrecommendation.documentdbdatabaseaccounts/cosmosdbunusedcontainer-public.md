<properties
    pageTitle="Consider taking action on your unused containers"
    description="Consider taking action on your unused containers"
    authors="dmliu16"
    ms.author="aoaft"
    articleId="893a1342-e1f6-49ec-97dc-c5c4471438c2_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Optimize Unused Containers and Geo-replications in Azure Cosmos DB
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "893a1342-e1f6-49ec-97dc-c5c4471438c2",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://cerebro.centralus.kusto.windows.net').database('Publish').GetAzureAdvisorUnusedContainersRecommendations",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Low",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBOptimizeUnusedContainer",
  "recommendationMetadataState": "Disabled",
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
  "learnMoreLink": "https://aka.ms/cosmosdb/usage-cost",
  "description": "Consider taking action on your unused containers",
  "longDescription": "This recommendation shows if Azure Cosmos DB containers and/or geo-replications are unused by looking at their usage data for the past 30 days. It is recommended to reduce the provisioned throughput to the configuration minimum if the stored data is still needed, or delete the container if it is no longer needed. If you have geo-replication enabled, ensure that you are using all the regions chosen.",
  "potentialBenefits": "Optimize Azure spend",
  "actions": [
    {
      "actionId": "1329e108-4139-4527-8270-f2886d64142b",
      "description": "Reduce throughput or consider deletion",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aa_cosmosdb_ru_action"
    },
    {
      "actionId": "50b42ebc-bdb6-491d-86ce-63d14eb3cd32",
      "description": "Verify that geo-replications are being used",
      "actionType": "Document",
      "documentLink": "https://aka.ms/cosmosdb/geo-replication"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "9cc91cb9-d271-4f76-b847-ec04aac16714",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "DatabaseAccountTemplateBladeForGlobalDb",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Optimize Unused Containers for Azure Cosmos DB",
  "additionalColumns": [
    {
      "name": "CollectionName",
      "title": "Collection Name"
    },
    {
      "name": "Region",
      "title": "Region"
    }
  ],
  "costSavingInfo": "*You can save up to the stated amount if you take the recommended action."
}
---
