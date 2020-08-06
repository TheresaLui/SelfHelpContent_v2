<properties
    pageTitle="Move your App Service resource to Standard or higher and use deployment slots"
    description="Move your App Service resource to Standard or higher and use deployment slots"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="59a83512-d885-4f09-8e4f-c796c71c686e_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="Compute_AppService"
/>
# Move your App Service resource to Standard or higher and use deployment slots
---
{
  "recommendationOfferingId": "c7f69506-5b4f-4751-b423-0095e68fad64",
  "recommendationOfferingName": "App Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "59a83512-d885-4f09-8e4f-c796c71c686e",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Web/sites",
  "recommendationFriendlyName": "AppServiceStandardOrHigher",
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
  "learnMoreLink": "https://aka.ms/ant-staging",
  "description": "Move your App Service resource to Standard or higher and use deployment slots",
  "longDescription": "You have deployed your application multiple times over the last week. Deployment slots help you manage changes and help you reduce deployment impact to your production web app.",
  "potentialBenefits": "Keep your app healthy while updating",
  "actions": [
    {
      "actionId": "AF800A4A-18DE-43F6-943A-6102375A0DF1",
      "description": "Move to Standard or higher SKU and create a slot",
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
      "actionId": "311A4485-9ACA-40E9-9B3B-7E254409528C",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Site Slots"
}
---
