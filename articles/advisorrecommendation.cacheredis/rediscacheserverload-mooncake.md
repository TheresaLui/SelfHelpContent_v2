<properties
    pageTitle="Improve your Cache and application performance when running with high server load"
    description="Improve your Cache and application performance when running with high server load"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="a25fccfd-854d-4c1a-9fae-aa0597a45e27_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="RedisCache_RedisCache"
/>
# Improve your Cache and application performance when running with high server load
---
{
  "recommendationOfferingId": "36d1891e-40d0-4dc5-bd43-ad946173dcd0",
  "recommendationOfferingName": "Redis Cache",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a25fccfd-854d-4c1a-9fae-aa0597a45e27",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Cache/redis",
  "recommendationFriendlyName": "RedisCacheServerLoad",
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
  "learnMoreLink": "https://aka.ms/redis/recommendations/cpu",
  "description": "Improve your Cache and application performance when running with high server load",
  "longDescription": "Cache instances perform best when not running under high server load which may cause them to become unresponsive, experience data loss, or become unavailable. Apply best practices to reduce the server load or scale to a different size or sku with more capacity.",
  "potentialBenefits": "Ensure optimal performance and high availability through best practices",
  "actions": [
    {
      "actionId": "e678a31b-df76-4c00-90a5-e5279321b310",
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
      "actionId": "f05492bc-1902-4f13-a8de-95a6402b6914",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Improve your Cache and application performance when running with high server load",
  "additionalColumns": [],
  "tip": "You can improve your Cache and application performance with high server load by scaling to a different size or sku"
}
---
