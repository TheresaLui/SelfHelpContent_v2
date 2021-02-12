<properties
    pageTitle="Upgrade to the latest version of the Azure Connected Machine agent"
    description="Upgrade to the latest version of the Azure Connected Machine agent"
    authors="hybridrpft"
    ms.author="hybridrpft"
    articleId="9d5717d2-4708-4e3f-bdda-93b3e6f1715b_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
    ownershipId="Compute_HybridResourceProvider"
/>
# Upgrade to the latest version of the Azure Connected Machine agent
---
{
  "recommendationOfferingId": "c567900d-5efa-4b08-a483-654108ca3b8a",
  "recommendationOfferingName": "Azure Arc enabled Servers",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "9d5717d2-4708-4e3f-bdda-93b3e6f1715b",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('hcrpprod.kusto.windows.net').database('hcrpprod').GetOutdatedArcAgents",
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.HybridCompute/machines",
  "recommendationFriendlyName": "ArcServerAgentVersion",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "hybridrpft@microsoft.com",
    "icm": {
      "routingId": "ADROCS://Recovery/HybridRP",
      "service": "Hybrid Resource Provider",
      "team": "Hybrid Resource Provider"
    },
    "serviceTreeId": "d41cab33-4a4f-4148-ab2f-2b5ff51bd406"
  },
  "ingestionClientIdentities": [],
  "version": 2.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/azure-arc/servers/manage-agent",
  "description": "Upgrade to the latest version of the Azure Connected Machine agent",
  "longDescription": "The Azure Connected Machine agent is updated regularly with bug fixes, stability enhancements, and new functionality. Upgrade your agent to the latest version for the best Azure Arc experience.",
  "potentialBenefits": "Improved stability and new functionality",
  "actions": [
    {
      "actionId": "26ea1be9-7b24-4812-8955-63b842a60e68",
      "description": "Upgrade agent",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/azure-arc/servers/manage-agent"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "5851ca0f-434c-4a89-a3e2-9b895f880f85",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_HybridCompute",
      "bladeName": "ResourceOverviewBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Upgrade the Azure Connected Machine agent",
  "additionalColumns": [
      {
          "name": "installedVersion",
          "title": "Installed version"
      },
      {
          "name": "latestVersion",
          "title": "Recommended version"
      }
  ]
}
---
