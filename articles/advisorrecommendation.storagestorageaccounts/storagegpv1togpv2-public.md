<properties
    pageTitle="Upgrade your Storage Account to General-purpose v2"
    description="Upgrade your Storage Account to General-purpose v2"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="1ef6e4c5-2caa-4528-a6e4-0db08a4d2872_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="StorageMediaEdge_XStore"
/>
# Upgrade your Storage Account to General-purpose v2
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "1ef6e4c5-2caa-4528-a6e4-0db08a4d2872",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "AzureStorageHUX.Data.StorageAdvisorUpgradeToGPv2",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "StorageGPv1ToGPv2",
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
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/storageaccounts",
  "description": "Upgrade your Storage Account to General-purpose v2",
  "longDescription": "General-purpose v2 (GPv2) accounts enables all the latest features at the lowest per gigabyte prices while retaining support for all APIs and features supported in General-purpose v1 (GPv1) and Blob storage accounts.",
  "potentialBenefits": "Take advantage of Storage's latest features and pricing model",
  "actions": [
    {
      "actionId": "7047aa48-8390-4cfc-bc53-79e21baef6e1",
      "description": "Upgrade Storage Account to GPv2",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "GeneralConfigurationBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "df597aa7-6096-4138-9344-3a485bb88c2a",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Upgrade Storage Account Kind to GPv2",
  "additionalColumns": []
}
---
