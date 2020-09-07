<properties
    pageTitle="Improve your Cache and application performance when running with high network bandwidth"
    description="Improve your Cache and application performance when running with high network bandwidth"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="a67201dd-6df0-4838-8258-5abf26adc8f6_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="RedisCache_RedisCache"
/>
# Improve your Cache and application performance when running with high network bandwidth
---
{
  "recommendationOfferingId": "36d1891e-40d0-4dc5-bd43-ad946173dcd0",
  "recommendationOfferingName": "Redis Cache",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a67201dd-6df0-4838-8258-5abf26adc8f6",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Cache/redis",
  "recommendationFriendlyName": "RedisCacheNetworkBandwidth",
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
  "learnMoreLink": "https://aka.ms/redis/recommendations/bandwidth",
  "description": "Improve your Cache and application performance when running with high network bandwidth",
  "longDescription": "Cache instances perform best when not running under high network bandwidth which may cause them to become unresponsive, experience data loss, or become unavailable. Apply best practices to reduce network bandwidth or scale to a different size or sku with more capacity.",
  "potentialBenefits": "Ensure optimal performance and high availability through best practices",
  "actions": [
    {
      "actionId": "d4aefa23-c7bb-46b1-a7c3-aa21575f088c",
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
      "actionId": "00013f1e-603e-41f4-947b-3a88db0f6393",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Improve your Cache and application performance when running with high network bandwidth",
  "additionalColumns": [],
  "tip": "You can improve your Cache and application performance with high network bandwith by scaling to a different size or sku"
}
---
