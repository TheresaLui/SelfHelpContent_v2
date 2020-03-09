<properties
    pageTitle="Add region to Azure Cosmos DB account"
    description="Add region to Azure Cosmos DB account"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="3d40e7fa-2ed5-4805-bb00-9c83596b55ad_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# Add region to Azure Cosmos DB account
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "3d40e7fa-2ed5-4805-bb00-9c83596b55ad",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbAddRegion",
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
  "learnMoreLink": "https://aka.ms/cosmos/globaldistribution",
  "description": "Add region to Azure Cosmos DB account",
  "longDescription": "We noticed traffic from a region that is not currently configured for your account. We recommend adding regions with traffic to improve latency for these requests and ensure availability in case of regional outages.",
  "potentialBenefits": "Improve latency and disaster recovery",
  "actions": [
    {
      "actionId": "b2008c3f-673d-43cd-9341-5b2ccaa631af",
      "description": "Add additional region",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "AddRemoveRegionsBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "edb4b8eb-1117-4a9f-b2c9-a7212651e091",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Add Region",
  "additionalColumns": [
    {
      "name": "regionName",
      "title": "Region"
    }
  ],
  "tip": "Add a region to your CosmosDB account to improve latency and disaster recovery"
}
---
