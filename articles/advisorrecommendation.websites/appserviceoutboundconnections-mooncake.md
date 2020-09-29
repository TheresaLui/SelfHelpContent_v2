<properties
    pageTitle="Check outbound connections from your App Service resource"
    description="Check outbound connections from your App Service resource"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="07f9a07d-9030-465c-89dc-b1f712334b83_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="Compute_AppService"
/>
# Check outbound connections from your App Service resource
---
{
  "recommendationOfferingId": "c7f69506-5b4f-4751-b423-0095e68fad64",
  "recommendationOfferingName": "App Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "07f9a07d-9030-465c-89dc-b1f712334b83",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Web/sites",
  "recommendationFriendlyName": "AppServiceOutboundConnections",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "antgrowth@microsoft.com",
    "icm": {
      "routingId": "AIMS://ANTST",
      "service": "App Service",
      "team": "antrec"
    },
    "serviceTreeId": "df36aee8-c644-400b-a0ab-fd0f1191211d"
  },
  "ingestionClientIdentities": [
  "dff79eea-93f9-44ae-8a0f-2f9f937f669e"
  ],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/antbc-socket_cn",
  "description": "Check outbound connections from your App Service resource",
  "longDescription": "Your app has opened too many TCP/IP socket connections. Exceeding ephemeral TCP/IP port connection limits can cause unexpected connectivity issues for your apps.",
  "potentialBenefits": "Better performance and lower cost",
  "actions": [
    {
      "actionId": "32F94739-6D5A-4CF9-82B0-0EE2341CF19C",
      "description": "Scale up your app",
      "actionType": "Blade",
      "extensionName": "WebsitesExtension",
      "bladeName": "SpecPickerFrameBlade",
       "metadata": {
        "id": "{serverFarmId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "C89F6A72-FBA3-4343-AF21-E7B04A157998",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Many outbound connections"
}
---
