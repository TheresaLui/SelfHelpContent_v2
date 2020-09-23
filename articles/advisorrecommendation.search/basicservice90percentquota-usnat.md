<properties
    pageTitle="You are close to exceeding storage quota of 2GB. Move to a Standard search service if you need more storage."
    description="After exceeding storage quota, indexing operations will stop working."
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="97b38421-f88c-4db0-b397-b2d81eff6630_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
    ownershipId="AzureSearch_AzureSearch"
/>
# You are close to exceeding storage quota of 2GB
---
{
  "recommendationOfferingId": "2be23fe8-3b59-46d2-bcb6-cdf01ede0583",
  "recommendationOfferingName": "Azure Search",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "97b38421-f88c-4db0-b397-b2d81eff6630",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://azsearchusnat.usnatwest.kusto.core.eaglex.ic.gov').database('AzureSearch').GetBasicServicesOver90PercentSizeQuota",
    "dataSource": "Kusto",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Search/searchServices",
  "recommendationFriendlyName": "BasicServiceStorageQuota90percent",
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
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/azs/search-limits-quotas-capacity",
  "description": "You are close to exceeding storage quota of 2GB. Create a Standard search service.",
  "longDescription": "You are close to exceeding storage quota of 2GB. Create a Standard search service. After exceeding storage quota, indexing operations will stop working.",
  "potentialBenefits": "capability to handle more data",
  "actions": [
    {
      "actionId": "06393e17-c527-45f8-9c40-1f6ea418e95c",
      "description": "Create an Azure Search service in the portal",
      "actionType": "Document",
      "documentLink": "https://aka.ms/azs/search-create-service-portal"
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
  "displayLabel": "You are close to exceeding storage quota of 2GB. Create a Standard search service for larger quota.",
  "additionalColumns": []
}
---