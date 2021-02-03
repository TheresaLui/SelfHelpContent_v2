<properties
    pageTitle="Consider scaling up your App Service Plan SKU to avoid memory exhaustion"
    description="Consider scaling up your App Service Plan SKU to avoid memory exhaustion"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="66d3137a-c4da-4c8a-b6b8-e03f5dfba66e_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
	ownershipId="Compute_AppService"
/>
# Consider scaling up your App Service Plan SKU to avoid memory exhaustion
---
{
  "recommendationOfferingId": "c7f69506-5b4f-4751-b423-0095e68fad64",
  "recommendationOfferingName": "App Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "66d3137a-c4da-4c8a-b6b8-e03f5dfba66e",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Web/sites",
  "recommendationFriendlyName": "AppServiceMemoryExhaustion",
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
  "bfc9fa96-6f4a-42b3-894f-29ff56b2bc89"
  ],
  "version": 1.1,
  "learnMoreLink": "https://aka.ms/antbc-memory_cn",
  "description": "Consider scaling up your App Service Plan SKU to avoid memory exhaustion",
  "longDescription": "The App Service Plan containing your app reached >85% memory allocated. High memory consumption can lead to runtime issues with your apps. Investigate which app in the App Service Plan is exhausting memory and scale up to a higher plan with more memory resources if needed.",
  "potentialBenefits": "Keep your app healthy",
  "actions": [
    {
      "actionId": "C8C48B3D-A198-475E-8927-C24FD9C90251",
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
      "actionId": "D0B7184F-5406-4C9A-8E91-3C44A6622866",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "High memory"
}
---
