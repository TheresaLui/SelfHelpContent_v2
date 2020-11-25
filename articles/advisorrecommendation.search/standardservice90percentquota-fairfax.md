<properties
    pageTitle="You are close to exceeding your available storage quota. Add additional partitions if you need more storage."
    description="After exceeding storage quota, you can still query, but indexing operations will no longer work."
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="b5a98691-da25-4fc3-a4f4-f9f0d35a42c6_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="AzureSearch_AzureSearch"
/>
# You are close to exceeding storage quota
---
{
  "recommendationOfferingId": "2be23fe8-3b59-46d2-bcb6-cdf01ede0583",
  "recommendationOfferingName": "Azure Search",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "b3efb46f-6d30-4201-98de-6492c1f8f10d",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://azsearchfairfax.kusto.usgovcloudapi.net').database('AzureSearch').GetStandardServicesOver90PercentSizeQuota",
    "dataSource": "Kusto",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Search/searchServices",
  "recommendationFriendlyName": "StandardServiceStorageQuota90percent",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "azuresearch_contact@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureSearch/Portal",
      "service": "Azure Search",
      "team": "Portal"
    },
    "serviceTreeId": "28d32201-d1ad-47ab-9a4a-3de2dcb6ea2a"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.1,
  "learnMoreLink": "https://aka.ms/azs/search-limits-quotas-capacity",
  "description": "You are close to exceeding your available storage quota. Add additional partitions if you need more storage.",
  "longDescription": "You are close to exceeding your available storage quota. Add additional partitions if you need more storage. After exceeding storage quota, you can still query, but indexing operations will no longer work.",
  "potentialBenefits": "Able to index additional data",
  "actions": [
    {
      "actionId": "06393e17-c527-45f8-9c40-1f6ea418e95c",
      "description": "Add partitions to your Azure Search service using the portal",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/search/search-manage"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "d9e03004-3e58-45cd-81e6-84c3e289883d",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "You are close to exceeding your available storage quota. Add additional partitions if you need more storage.",
  "additionalColumns": []
}
---
