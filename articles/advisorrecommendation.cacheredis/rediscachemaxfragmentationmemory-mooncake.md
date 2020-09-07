<properties
    pageTitle="Availability may be impacted from high memory fragmentation. Increase fragmentation memory reservation to avoid potential impact."
    description="Availability may be impacted from high memory fragmentation. Increase fragmentation memory reservation to avoid potential impact."
    authors="suryaren"
    ms.author="suryaren"
    articleId="7c380315-6ad9-4fb2-8930-a8aeb1d6241b_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="RedisCache_RedisCache"
/>
# Availability may be impacted from high memory fragmentation. Increase fragmentation memory reservation to avoid potential impact.
---
{
  "recommendationOfferingId": "36d1891e-40d0-4dc5-bd43-ad946173dcd0",
  "recommendationOfferingName": "Redis Cache",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "7c380315-6ad9-4fb2-8930-a8aeb1d6241b",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Cache/redis",
  "recommendationFriendlyName": "RedisCacheMemoryFragmentation",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "AzureCacheFT@microsoft.com",
    "icm": {
      "routingId": "RedisS1S2BusinessHoursOnly",
      "service": "Windows Azure Cache",
      "team": "Redis S1S2 BusinessHoursOnly"
    },
    "serviceTreeId": "59fe8ab9-6707-4b3c-afb0-f5ed4214b531"
  },
  "ingestionClientIdentities": [
    "91ffa3d2-0a02-46d7-9c21-806c2f81271a"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "http://aka.ms/redis/recommendations/memory-policies",
  "description": "Availability may be impacted from high memory fragmentation. Increase fragmentation memory reservation to avoid potential impact.",
  "longDescription": "Fragmentation and memory pressure can cause availability incidents during a failover or management operations. Increasing reservation of memory for fragmentation helps in reducing the cache failures when running under high memory pressure. Memory for fragmentation can be increased via maxfragmentationmemory-reserved setting available in advanced settings blade.",
  "potentialBenefits": "Avoid availability incidents when your cache has high memory fragmentation",
  "testData":"cabd7983-99cd-4ec6-b92c-2b10e52c2f58,/subscriptions/cabd7983-99cd-4ec6-b92c-2b10e52c2f58/resourceGroups/Investigate-Redis/providers/Microsoft.Cache/Redis/test123",
  "actions": [
    {
      "actionId": "b92530c0-75c9-4398-a099-3d97a9760a69",
      "description": "Increase your max fragmentation memory reservation",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "redisConfig"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "b92530c0-75c9-4398-a099-3d97a9760a69",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Increase fragmentation memory reservation",
  "additionalColumns": [],
  "tip": "You can avoid availability incidents by increasing fragmentation memory reservation"
}
---