<properties
    pageTitle="Delete and recreate your pool to remove a deprecated internal component"
    description="Delete and recreate your pool to remove a deprecated internal component"
    authors="pkshultz"
    ms.author="pkshultz"
    articleId="a49b0685-56d6-468d-b879-7e021a2395e3_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    productPesIds="15614"
    ownershipId="Compute_Batch"
/>
# Recreate your pool
---
{
  "recommendationOfferingId": "58aa8ff2-5d53-444a-8026-1610fb23c30f",
  "recommendationOfferingName": "Batch",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a49b0685-56d6-468d-b879-7e021a2395e3",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://azurebatch.kusto.windows.net').database('azurebatchprod').AzureAdvisor_PoolServerPools",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Batch/batchAccounts",
  "recommendationFriendlyName": "RecreatePool",
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
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/batch_deprecatedcomponent_learnmore",
  "description": "Delete and recreate your pool to remove a deprecated internal component",
  "longDescription": "Your pool is using a deprecated internal component. Please delete and recreate your pool for improved stability and performance.",
  "potentialBenefits": "Improved stability and performance",
  "actions": [
    {
      "actionId": "b3f667f3-a99e-48f3-a324-eb9ab4f19910",
      "actionType": "Document",
      "description": "Delete and recreate your pool.",
      "documentLink": "https://aka.ms/batch_deprecatedcomponent_learnmore"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "9cb8eb71-a71f-4db5-883e-7a2ed34b374a",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Deprecated internal component on Batch pools",
  "additionalColumns": [
	{
      "name": "poolName",
      "title": "Pool name"
    }
  ],
  "tip": "Please delete and recreate your pool for improved stability and performance."
}
---
