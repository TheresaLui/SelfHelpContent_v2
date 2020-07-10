<properties
    pageTitle="Prevent hitting subscription limit for maximum storage accounts"
    description="Prevent hitting subscription limit for maximum storage accounts"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="a0ad4f8c-f904-4b11-955d-e0044473c5fa_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="StorageMediaEdge_XStore"
/>
# Prevent hitting subscription limit for maximum storage accounts
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a0ad4f8c-f904-4b11-955d-e0044473c5fa",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "azurestorage.data.storageadvisoraccountscaletargetmooncake",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "StorageAccountScaleTarget",
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
  "learnMoreLink": "https://aka.ms/subscalelimit_cn",
  "description": "Prevent hitting subscription limit for maximum storage accounts",
  "longDescription": "A region can support a maximum of 250 storage accounts per subscription. You have either already reached or are about to reach that limit. If you reach that limit, you will be unable to create any more storage accounts in that subscription/region combination. Please evaluate the recommended action below to avoid hitting the limit.",
  "potentialBenefits": "Ensure you do not reach the limit that can prevent you from creating additional storage accounts",
  "actions": [
    {
      "actionId": "937a7f37-6591-4e89-bb11-4866a83531f3",
      "description": "Design for fewer accounts per subscription per region ",
      "actionType": "Document",
      "documentLink": "https://aka.ms/subscalelimit_cn"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "8615139e-0106-4611-a10c-e5b6c13b8e5a",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "region": "{region}"
      }
    }
  },
  "displayLabel": "Prevent hitting subscription limit for maximum storage accounts",
  "additionalColumns": []
}
---
