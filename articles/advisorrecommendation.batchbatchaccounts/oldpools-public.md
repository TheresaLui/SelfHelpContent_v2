<properties
    pageTitle="Recreate your pool to get the latest node agent updates and bug fixes"
    description="Recreate your pool to get the latest node agent updates and bug fixes"
    authors="pkshultz,smith1511"
    ms.author="pkshultz,smith1511"
    articleId="962f2d6d-b2c7-4c48-9e61-2a857051815d_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    productPesIds="15614"
    ownershipId="Compute_Batch"
/>
# Recreate your pool to get the latest node agent updates and bug fixes
---
{
  "recommendationOfferingId": "58aa8ff2-5d53-444a-8026-1610fb23c30f",
  "recommendationOfferingName": "Batch",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "962f2d6d-b2c7-4c48-9e61-2a857051815d",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://azurebatch.kusto.windows.net').database('azurebatchprod').AzureAdvisor_OldPools",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Batch/batchAccounts",
  "recommendationFriendlyName": "OldPool",
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
  "version": 7.0,
  "learnMoreLink": "https://aka.ms/batch_oldpool_learnmore",
  "description": "Recreate your pool to get the latest node agent features and fixes",
  "longDescription": "Your pool has an old node agent. Consider recreating your pool to get the latest node agent updates and bug fixes.",
  "potentialBenefits": "Improved functionality and stability",
  "actions": [
    {
      "actionId": "f2e12464-8d37-40e5-80e6-1567410f18b6",
      "actionType": "Document",
      "description": "Recreate your pool, or temporarily resize it to 0 nodes.",
      "documentLink": "https://aka.ms/batch_oldpool_learnmore"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "669798c8-09f8-48bf-90ec-f11d35f9356d",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Old node agents on Batch pools",
  "additionalColumns": [
    {
      "name": "poolName",
      "title": "Pool name"
    },
	{
      "name": "nodeAgentAge",
      "title": "Node agent age"
    }
  ],
  "tip": "Consider recreating old pools to get the latest node agent, which includes the latest updates and bug fixes. Alternatively, scale the pool down to 0 nodes and then resize back up."
}
---
