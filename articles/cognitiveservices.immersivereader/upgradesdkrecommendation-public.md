<properties
    pageTitle="Upgrade to the latest SDK version"
    description="Upgrade to the latest SDK version"
    authors="ltcrew"
    ms.author="ltcrew"
    articleId="936111C6-01C1-4448-A44A-0C36208E64AC_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, ussec, usnat"
    ownershipId="AzureCogSvc_CognitiveServices"
/>

# Recommend upgrading to a more recent SDK version.
---
{
  "recommendationOfferingId": "2b95a890-ee31-4acb-8eaf-912676d642af",
  "recommendationOfferingName": "Immersive Reader",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "10DF9B5E-41B9-4DD1-BFE0-44177F9156E5",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('cogsvcaria.eastus2.kusto.windows.net').database('072b8d92ee094f6aa68cc5cf127fff4b').AzureAdvisor_UpgradeSDK",
    "dataSource": "Kusto",
    "refreshInterval": "2:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Low",
  "recommendationResourceType": "Microsoft.CognitiveServices/accounts",
  "recommendationFriendlyName": "ImmersiveReaderSDKRecommendation",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "ltcrew@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/CogServ/ImmerReader",
      "service": "Cognitive Services",
      "team": "Immersive Reader"
    },
    "serviceTreeId": "53e1b385-c6b4-4ebb-859a-54b8f78bdd61"
  },
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/ImmersiveReaderAzureAdvisorSDKLearnMore",
  "description": "Upgrade to the latest version of the Immersive Reader SDK",
  "longDescription": "We have identified resources under this subscription using outdated versions of the Immersive Reader SDK. Using the latest version of the Immersive Reader SDK provides you with updated security, performance and an expanded set of features for customizing and enhancing your integration experience.",
  "potentialBenefits": "Improved security, performance and support for new features.",
  "tip": "Regularly upgrade the Immersive Reader SDK version to access updates, enhancements and new features.",
  "displayLabel": "Upgrade to the latest version of the Immersive Reader SDK",
  "additionalColumns": [
    {
      "name": "CurrentSDKVersion",
      "title": "Current SDK Version"
    }
  ],
  "supportedSDKLanguages": ["JS"],
  "actions": [
    {
      "actionId": "C7D442B0-3E9C-43DD-8495-E4FFD2ED8B1E",
      "description": "Upgrade your current Immersive Reader SDK to the latest version, {version}",
      "actionType": "Document",
      "documentLink": "{releaseNotes}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "80A8A7E9-80CE-4C2C-A3DE-6380D9882AB5",
      "description": "Check the resource",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_ProjectOxford",
      "bladeName": "ResourceBlade",
      "metadata": {"id": "{resourceId}"}
    }
  },
  "testData": "e27fbfa4-da13-4cb3-9aaa-3929b702a9db,/subscriptions/e27fbfa4-da13-4cb3-9aaa-3929b702a9db/resourceGroups/Cogsvcs/providers/Microsoft.CognitiveServices/accounts/ImmersiveReader_S0_SF_WestUS2,JS,1.1.0,https://aka.ms/ImmersiveReaderAzureAdvisorSDKLearnMore,https://aka.ms/ImmersiveReaderSDKReleaseNotes,{\"CurrentSDKVersion\":\"1.0.0\"}"
}
---
