<properties
    pageTitle="Consider scaling out your App Service Plan to avoid CPU exhaustion"
    description="Consider scaling out your App Service Plan to avoid CPU exhaustion"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="1294987d-c97d-41d0-8fd8-cb6eab52d87b_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# Consider scaling out your App Service Plan to avoid CPU exhaustion
---
{
  "recommendationOfferingId": "c7f69506-5b4f-4751-b423-0095e68fad64",
  "recommendationOfferingName": "App Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "1294987d-c97d-41d0-8fd8-cb6eab52d87b",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Web/sites",
  "recommendationFriendlyName": "AppServiceCPUExhaustion",
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
  "95ef4a4a-35e3-48f4-9313-aa225c47e995",
  "2f750bee-e9a6-4ecf-881d-e0a2d3ee2f46",
  "adf3bc1f-f9ab-49a3-b81c-06a36582c68f"
  ],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/antbc-cpu",
  "description": "Consider scaling out your App Service Plan to avoid CPU exhaustion",
  "longDescription": "Your App reached >90% CPU over the last couple of days. High CPU utilization can lead to runtime issues with your apps, to solve this you could scale out your app.",
  "potentialBenefits": "Keep your app healthy",
  "actions": [
    {
      "actionId": "6943BC86-0B3C-495D-8F23-11BE8884BA56",
      "description": "Scale out your app",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Monitoring",
      "bladeName": "AutoScaleSettingsBlade",
       "metadata": {
        "WebHostingPlanId": "{serverFarmId}",
	"resourceId": "{serverFarmId}",
	"apiVersion": "2015-08-01"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "B707F709-B597-4E43-9A53-AD7A16F4D52A",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "High CPU"
}
---
