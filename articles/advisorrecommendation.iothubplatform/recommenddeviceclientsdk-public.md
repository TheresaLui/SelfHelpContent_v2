<properties
    pageTitle="Upgrade PreLTS Iot Hub Device Client SDK"
    description="Recommendation to upgrade PreLTS Iot Hub Device Client SDK"
    ms.author="iothubcoresvc"
    articleId="d448c687-b808-4143-bbdc-02c35478198a_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="AzureIotHub_IotPlatform"
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
    "refreshInterval": "06:00:00	"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Devices/IotHubs",
  "recommendationFriendlyName": "UpgradeDeviceClientSdk",
  "recommendationMetadataState": "Disabled",
  "owner": {
    "email": "iothubcoresvc@microsoft.com",
    "icm": {
      "routingId": "adrocs://Recovery/DhubMds",
      "service": "Azure Iot Hub",
      "team": "IoTHub"
    },
    "serviceTreeId": "aeaf65ef-e107-4f59-b33e-7226c0415cd2"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/iothubsdk",
  "description": "Upgrade to a supported version of the SDK",
  "longDescription": "Some or all of your devices are using outdated SDK and we recommend you upgrade to a supported version of SDK. See the details in the recommendation.",
  "potentialBenefits": "Ensure business continuity with supported SDK for your devices",
  "supportedSDKLanguages": [],
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
      "actionId": "",
      "actionType": "",
      "extensionName": "",
      "bladeName": "",
      "metadata": {},
      "documentLink": ""
    }
  },
  "displayLabel": "Upgrade Device Client SDK",
  "additionalColumns": [
    {
      "name": "Language",
      "title": "SDK Language"
    },
    {
      "name": "MinimumSupportedVersion",
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
  "tip": "",
  "testData": "C306C958-55C4-41A2-86F4-53F1657A726A,/SUBSCRIPTIONS/C306C958-55C4-41A2-86F4-53F1657A726A/RESOURCEGROUPS/DPS-RUNNERS/PROVIDERS/MICROSOFT.DEVICES/IOTHUBS/DPS-SU-RUNNER-HUB-MWH001-2,\"{\"\"Language\"\":\"\"Java\"\",\"\"MinimumSupportedVersion\"\":\"\"1.22.0\"\",\"\"RecommendedActionLearnMore\"\":\"\" https://github.com/Azure/azure-iot-sdk-csharp\"\",\"\"ReleaseNotes\"\":\"\"https://github.com/Azure/azure-iot-sdk-csharp/releases\"\",\"\"hubName\"\":\"\"TestHub\"\",\"\"deviceCount\"\":\"\"102\"\"}\"""
}
---
