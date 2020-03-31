<properties
    pageTitle="Configure your Azure Cosmos DB applications to use Direct connectivity in the SDK"
    description="Configure your Azure Cosmos DB applications to use Direct connectivity in the SDK"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="75c8c891-46d2-41fa-a81c-84e870a139a9_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# Configure your Azure Cosmos DB applications to use Direct connectivity in the SDK
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "75c8c891-46d2-41fa-a81c-84e870a139a9",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbGatewayMode",
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
  "learnMoreLink": "https://aka.ms/cosmosdb/networking-performance",
  "description": "Configure your Azure Cosmos DB applications to use Direct connectivity in the SDK",
  "longDescription": "We noticed that your Azure Cosmos DB applications are using Gateway mode via the Cosmos DB .NET or Java SDKs. We recommend switching to Direct connectivity for lower latency and higher scalability.",
  "potentialBenefits": "Improve latency and high availability of your applications",
  "actions": [
    {
      "actionId": "8d53c5ee-d517-4d13-8df8-cac65d6f5a56",
      "description": "Configure to use Direct connectivity",
      "actionType": "Document",
      "documentLink": "https://aka.ms/cosmosdb/networking-performance"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "b4f76069-a635-4dfa-a6bf-8fac5ff253e3",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Configure your applications to use Direct connectivity in the SDK",
  "additionalColumns": []
}
---
