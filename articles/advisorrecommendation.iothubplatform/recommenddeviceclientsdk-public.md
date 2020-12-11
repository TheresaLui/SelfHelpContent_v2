<properties
    pageTitle="Upgrade PreLTS Iot Hub Device Client SDK"
    description="Recommendation to upgrade PreLTS Iot Hub Device Client SDK"
    ms.author="iothubcoresvc"
    articleId="d448c687-b808-4143-bbdc-02c35478198a_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
    ownershipId="AzureIot_IotHub"
/>
# Recommendation to upgrade PreLTS Iot Hub Device Clients SDK
---
{
  "recommendationOfferingId": "e8bbf6c9-ae5d-4763-afd3-9cb823dcf6a3",
  "recommendationOfferingName": "Iot Hub",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "d448c687-b808-4143-bbdc-02c35478198a",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://iothub.kusto.windows.net').database('IotHub').PreLtsClientSdkAdvisor",
    "dataSource": "Kusto",
    "refreshInterval": "06:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Devices/IotHubs",
  "recommendationFriendlyName": "UpgradeDeviceClientSdk",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "iothubcoresvc@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/AzureIoTHub",
      "service": "Azure Iot Hub",
      "team": "IoTHub"
    },
    "serviceTreeId": "aeaf65ef-e107-4f59-b33e-7226c0415cd2"
  },
  "ingestionClientIdentities": [],
  "version": 1.8,
  "learnMoreLink": "https://aka.ms/iothubsdk",
  "description": "Upgrade to a supported version of the SDK",
  "longDescription": "Some or all of your devices are using outdated SDK and we recommend you upgrade to a supported version of SDK. See the details in the recommendation.",
  "potentialBenefits": "Ensure business continuity with supported SDK for your devices",
  "supportedSDKLanguages": ["Java", "C", "C#", "Python", "Node"],
  "actions": [
    {
      "actionId": "6d00a3ba-5303-4d23-bb23-a8851f6c1340",
      "description": "View to learn more about recommended action",
      "actionType": "Document",
      "documentLink": "{RecommendedActionLearnMore}"
    },
    {
      "actionId": "3c2445ba-3365-45ec-831c-512665ea4105",
      "description": "View {version} release notes",
      "actionType": "Document",
      "documentLink": "{ReleaseNotes}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "58cb3e4b-dfff-4758-b953-1fa2ae9b761b",
      "actionType": "Document",
      "description": "Upgrade to a supported version of the SDK",
      "documentLink": "https://aka.ms/iothubsdk"
    }
  },
  "displayLabel": "Upgrade Device Client SDK",
  "additionalColumns": [
    {
      "name": "Language",
      "title": "SDK Language"
    },
    {
      "name": "Version",
      "title": "Minimum Recommended Version"
    },
    {
        "name": "hubName",
        "title": "Hub Name"
    },
    {
        "name": "deviceCount",
        "title": "Count of devices using outdated SDK version"
    }
  ],
  "tip": ""
}
---
