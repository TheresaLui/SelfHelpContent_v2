<properties
    pageTitle="Use deployment slots for your App Service resource"
    description="Use deployment slots for your App Service resource"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="0dc165fd-69bf-468a-aa04-a69377b6feb0_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="Compute_AppService"
/>
# Use deployment slots for your App Service resource
---
{
  "recommendationOfferingId": "c7f69506-5b4f-4751-b423-0095e68fad64",
  "recommendationOfferingName": "App Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "0dc165fd-69bf-468a-aa04-a69377b6feb0",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Web/sites",
  "recommendationFriendlyName": "AppServiceUseDeploymentSlots",
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
  "learnMoreLink": "https://aka.ms/ant-staging_fn",
  "description": "Use deployment slots for your App Service resource",
  "longDescription": "You have deployed your application multiple times over the last week. Deployment slots help you manage changes and help you reduce deployment impact to your production web app.",
  "potentialBenefits": "Keep your app healthy while updating",
  "actions": [
    {
      "actionId": "CE929CED-2952-47E5-A9EA-B29FD3358884",
      "description": "Create a new slot",
      "actionType": "Blade",
      "extensionName": "WebsitesExtension",
      "bladeName": "websiteSlotsListBlade",
       "metadata": {
        "resourceUri": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "FD2C0CBA-871A-460E-9208-B864BB6B0D47",
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
