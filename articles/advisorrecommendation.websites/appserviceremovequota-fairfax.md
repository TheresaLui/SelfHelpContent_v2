<properties
    pageTitle="Scale up your App Service resource to remove the quota limit"
    description="Scale up your App Service resource to remove the quota limit"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="78c5ab69-858a-43ca-a5ac-4ca6f9cdc30d_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="Compute_AppService"
/>
# Scale up your App Service resource to remove the quota limit
---
{
  "recommendationOfferingId": "c7f69506-5b4f-4751-b423-0095e68fad64",
  "recommendationOfferingName": "App Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "78c5ab69-858a-43ca-a5ac-4ca6f9cdc30d",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Web/sites",
  "recommendationFriendlyName": "AppServiceRemoveQuota",
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
  "484db53f-83ae-4f6a-a922-931561863edb"
  ],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/ant-asp_ff",
  "description": "Scale up your App Service resource to remove the quota limit",
  "longDescription": "Your app is part of a shared App Service plan and has met its quota multiple times. After meeting a quota, your web app can’t accept incoming requests. To remove the quota, upgrade to a Standard plan.",
  "potentialBenefits": "Keep your app healthy",
  "actions": [
    {
      "actionId": "0AE02C23-3769-4967-AFD6-F0B01C5B3596",
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
      "actionId": "BAB9F0FE-0A40-4A54-A8B7-4C632EEE47EF",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Exceeded quota limit"
}
---
