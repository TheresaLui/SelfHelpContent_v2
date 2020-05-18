<properties
    pageTitle="Upgrade to the latest API version"
    description="Upgrade to the latest API version"
    authors="pkshultz,jafreck"
    ms.author="pkshultz,jafreck"
    articleId="bbc3f0f1-85b7-4bcb-b474-0e02571eb5fa_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    productPesIds="15614"
    ownershipId="Compute_Batch"
/>
# Upgrade to the latest API version
---
{
  "recommendationOfferingId": "58aa8ff2-5d53-444a-8026-1610fb23c30f",
  "recommendationOfferingName": "Batch",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "bbc3f0f1-85b7-4bcb-b474-0e02571eb5fa",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://azurebatchff.kusto.usgovcloudapi.net').database('azurebatchprod').AzureAdvisor_toBeDeprecatedAPI",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Batch/batchAccounts",
  "recommendationFriendlyName": "UpgradeAPI",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "xcompute@microsoft.com",
    "icm": {
      "routingId": "MDM://AZURE TASK/DOTD",
      "service": "Azure Batch",
      "team": "DOTD"
    },
    "serviceTreeId": "484d96f7-5abc-4961-ab67-7d0f7edc620a"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 4.0,
  "learnMoreLink": "https://aka.ms/batch_deprecatedapi_learnmore",
  "description": "Upgrade to the latest API version to ensure your Batch account remains operational.",
  "longDescription": "In the past 14 days, you have invoked a Batch management or service API version that is scheduled for deprecation. Upgrade to the latest API version to ensure your Batch account remains operational.",
  "potentialBenefits": "Improved functionality and stability",
  "actions": [
    {
      "actionId": "6ffb924a-d3c1-4ea3-80f4-7945d53fe6ce",
      "actionType": "Document",
      "description": "Upgrade to the latest API version.",
      "documentLink": "https://aka.ms/batch_deprecatedapi_learnmore"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "8176f6cd-60eb-4bfc-ab13-e6052e47f7aa",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "API versions scheduled for deprecation",
  "additionalColumns": [
    {
      "name": "apiType",
      "title": "API Type"
    },
    {
      "name": "sdkType",
      "title": "SDK Type"
    },
    {
      "name": "version",
      "title": "Current Version"
    },
    {
      "name": "minimumRecommendedVersion",
      "title": "Minimum Recommended Version"
    }
  ],
  "tip": "Upgrade to the latest API version to ensure your Batch account remains operational."
}
---
