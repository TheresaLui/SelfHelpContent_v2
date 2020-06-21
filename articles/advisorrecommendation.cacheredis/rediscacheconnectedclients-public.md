<properties
    pageTitle="Improve your Cache and application performance when running with many connected clients"
    description="Improve your Cache and application performance when running with many connected clients"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="a5ab10c5-424a-4818-9fba-ddca1eee531a_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="RedisCache_RedisCache"
/>
# Improve your Cache and application performance when running with many connected clients
---
{
  "recommendationOfferingId": "36d1891e-40d0-4dc5-bd43-ad946173dcd0",
  "recommendationOfferingName": "Redis Cache",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a5ab10c5-424a-4818-9fba-ddca1eee531a",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Cache/redis",
  "recommendationFriendlyName": "RedisCacheConnectedClients",
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
    "91ffa3d2-0a02-46d7-9c21-806c2f81271a"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/redis/recommendations/connections",
  "description": "Improve your Cache and application performance when running with many connected clients",
  "longDescription": "Cache instances perform best when not running under high server load which may cause them to become unresponsive, experience data loss, or become unavailable. Apply best practices to reduce the server load or scale to a different size or sku with more capacity.",
  "potentialBenefits": "Ensure optimal performance and high availability through best practices",
  "actions": [
    {
      "actionId": "52d59fe3-1dfa-431b-833e-3043ea4bf180",
      "description": "Scale to a different size or sku",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "scaleUp"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "d15da33b-8390-49f6-9a67-4c068a075a84",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Improve your Cache and application performance when running with many connected clients",
  "additionalColumns": [],
  "tip": "You can improve your Cache and application performance when running with many connected clients by scaling to a different size or sku"
}
---
