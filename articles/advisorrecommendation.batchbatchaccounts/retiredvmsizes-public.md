<properties
    pageTitle="Delete and recreate your pool using a VM size that will soon be retired"
    description="Delete and recreate your pool using a VM size that will soon be retired"
    authors="pkshultz"
    ms.author="pkshultz"
    articleId="48ae14cb-10de-4bd9-a005-5c25f498649b_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public,Usnat,USsec"
    productPesIds="15614"
    ownershipId="Compute_Batch"
/>
# Recreate your pool
---
{
  "recommendationOfferingId": "58aa8ff2-5d53-444a-8026-1610fb23c30f",
  "recommendationOfferingName": "Batch",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "48ae14cb-10de-4bd9-a005-5c25f498649b",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://azurebatch.kusto.windows.net').database('azurebatchprod').AzureAdvisor_A8toA11Pools",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Batch/batchAccounts",
  "recommendationFriendlyName": "RemoveA8_A11Pools",
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
  "version": 3.0,
  "learnMoreLink": "https://aka.ms/batch_a8_a11_retirement_learnmore",
  "description": "Delete and recreate your pool using a VM size that will soon be retired",
  "longDescription": "Your pool is using A8-A11 VMs, which are set to be retired in March 2021. Please delete your pool and recreate it with a different VM size.",
  "potentialBenefits": "Avoid potential interruptions",
  "actions": [
    {
      "actionId": "8edfb036-cb3a-4dba-ae80-3e405c68cabd",
      "actionType": "Document",
      "description": "Delete your pool and recreate it with a different VM size",
      "documentLink": "https://aka.ms/batch_a8_a11_retirement_learnmore"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "09b32dc9-0409-4445-a004-8e2a3bec7e3f",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Pools using a VM size that will be retired soon",
  "additionalColumns": [
	{
      "name": "poolName",
      "title": "Pool name"
    }
  ],
  "tip": "Delete your pool and recreate it with a different VM size to avoid potential interruptions when the VM size is retired."
}
---
