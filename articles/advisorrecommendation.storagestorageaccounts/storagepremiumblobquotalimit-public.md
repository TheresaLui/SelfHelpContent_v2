<properties
    pageTitle="Use Managed Disks for storage accounts reaching capacity limit"
    description="Use Managed Disks for storage accounts reaching capacity limit"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="d42d751d-682d-48f0-bc24-bb15b61ac4b8_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="StorageMediaEdge_XStore"
/>
# Use Managed Disks for storage accounts reaching capacity limit
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "d42d751d-682d-48f0-bc24-bb15b61ac4b8",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "AzureStorage.Data.StorageAdvisorPremiumBlobQuotaLimitPulic",
    "dataSource": "Cosmos",
    "refreshInterval": "3.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "StoragePremiumBlobQuotaLimit",
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
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/premium_blob_quota",
  "description": "Use Managed Disks for storage accounts reaching capacity limit",
  "longDescription": "We have identified that you are using Premium SSD Unmanaged Disks in Storage account(s) that are about to reach Premium Storage capacity limit. To avoid failures when this limit is reached, we recommend you migrate to Managed Disks that does not have account capacity limit. This migration can be done through the portal in less than 5 minutes.",
  "potentialBenefits": "Avoid scale issues when account reaches capacity limit",
  "actions": [
    {
      "actionId": "eb8febf0-86e1-4fc4-9eef-95ab472ef4e2",
      "description": "Migrate existing Premium Disk to Managed Disk",
      "actionType": "Document",
      "documentLink": "https://aka.ms/migrate_to_md"
    },
    {
      "actionId": "7f497644-8e84-4450-a215-4da94290e984",
      "description": "Learn benefits of and use Managed Disks for new VMs",
      "actionType": "Document",
      "documentLink": "https://aka.ms/md_overview"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "3fd3adae-94f5-4fef-9a3e-aac8b4de18ed",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Migrate Premium Disks from Unmanaged to Managed",
  "additionalColumns": []
}
---

