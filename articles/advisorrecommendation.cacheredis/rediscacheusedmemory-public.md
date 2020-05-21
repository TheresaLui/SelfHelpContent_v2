<properties
    pageTitle="Improve your Cache and application performance when running with high memory pressure"
    description="Improve your Cache and application performance when running with high memory pressure"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="16d0cf25-463d-4a20-8f18-d8d71edf92e3_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="RedisCache_RedisCache"
/>
# Improve your Cache and application performance when running with high memory pressure
---
{
  "recommendationOfferingId": "36d1891e-40d0-4dc5-bd43-ad946173dcd0",
  "recommendationOfferingName": "Redis Cache",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "16d0cf25-463d-4a20-8f18-d8d71edf92e3",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Cache/redis",
  "recommendationFriendlyName": "RedisCacheUsedMemory",
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
  "learnMoreLink": "https://aka.ms/redis/recommendations/memory",
  "description": "Improve your Cache and application performance when running with high memory pressure",
  "longDescription": "Cache instances perform best when not running under high memory pressure which may cause them to become unresponsive, experience data loss, or become unavailable. Apply best practices to reduce used memory or scale to a different size or sku with more capacity.",
  "potentialBenefits": "Ensure optimal performance and high availability through best practices",
  "actions": [
    {
      "actionId": "9262e05c-15a0-4bdf-bf1a-ba5391db50d7",
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
      "actionId": "65382d3f-8dc9-4107-8979-6c4f53f9d552",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Improve your Cache and application performance when running with high memory pressure",
  "additionalColumns": [],
  "tip": "You can improve your Cache and application performance with high memory pressure by scaling to a different size or sku"
}
---
