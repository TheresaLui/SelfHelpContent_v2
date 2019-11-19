<properties
    pageTitle="Availability may be impacted from high memory fragmentation. Increase the value of your fragmentation memory reservation to avoid potential impact."
    description="Availability may be impacted from high memory fragmentation. Increase the value of your fragmentation memory reservation to avoid potential impact."
    authors="AzureCacheFT"
    ms.author="AzureCacheFT"
    articleId="7c380315-6ad9-4fb2-8930-a8aeb1d6241b_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Availability may be impacted from high memory fragmentation. Increase the value of your fragmentation memory reservation to avoid potential impact.
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
  "learnMoreLink": "http://aka.ms/redis/recommendations/memory-policies",
  "description": "Availability may be impacted from high memory fragmentation. Increase the value of your fragmentation memory reservation to avoid potential impact.",
  "longDescription": "Avaliability may be impacted due to high memory fragmentation. Please consider setting maxfragmentationmemory-reserved",
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
  "displayLabel": "Avoid availability incidents from high memory fragmentation by increasing the value of your fragmentation memory reservation",
  "additionalColumns": [],
  "tip": "You can avoid availability incidents by increasing the value of your fragmentation memory reservation"
}
---