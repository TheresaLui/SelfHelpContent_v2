<properties
    pageTitle="Migrate your data from Standard Storage account to Premium Storage account"
    description="Migrate your data from Standard Storage account to Premium Storage account"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="ad488f61-5ada-4c72-8296-56ea29955552_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="StorageMediaEdge_XStore"
/>
# Migrate your data from Standard Storage account to Premium Storage account
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "ad488f61-5ada-4c72-8296-56ea29955552",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "AzureAdvisor.MigrateToPremiumStorageDaily",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "MigrateToPremiumStorage",
  "recommendationMetadataState": "Disabled",
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
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.1,
  "learnMoreLink": "https://aka.ms/aa_premiumstg_migrate_learnmore",
  "description": "Migrate your data from Standard Storage account to Premium Storage account",
  "longDescription": "We noticed that there is a high volume of transactions on your storage account. We recommend you to migrate to Premium Storage (SSD based) to boost your performance on Page Blobs/Unmanaged Disks.",
  "potentialBenefits": "Improve your performance with lower latency and provisioned performance",
  "actions": [
    {
      "actionId": "36328c99-79de-47db-8ec5-70ec616c19ae",
      "description": "Migrate from Standard Storage to Premium Storage",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aa_premiumstg_migrate_action1"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "a419b464-2aec-4901-a63a-813b4acd16f9",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Migrate from Standard Storage to Premium Storage",
  "additionalColumns": []
}
---
