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
  "recommendationImpact": "Low",
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
  "version": 2.5,
  "learnMoreLink": "https://aka.ms/iothubsdk",
  "description": "Upgrade device client SDK to a supported version for IotHub",
  "longDescription": "Some or all of your devices are using outdated SDK and we recommend you upgrade to a supported version of SDK. See the details in the recommendation.",
  "potentialBenefits": "Ensure business continuity with supported SDK for your devices",
  "supportedSDKLanguages": ["Java", "C", "C#", "Python", "Node"],
  "actions": [
    {
      "actionId": "6d00a3ba-5303-4d23-bb23-a8851f6c1340",
      "description": "View to learn more about recommended action",
      "actionType": "Document",
      "documentLink": "{recommendedActionLearnMore}"
    },
    {
      "actionId": "3c2445ba-3365-45ec-831c-512665ea4105",
      "description": "View {language} SDK {version} release notes",
      "actionType": "Document",
      "documentLink": "{releaseNotes}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "58cb3e4b-dfff-4758-b953-1fa2ae9b761b",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_IotHub",
      "bladeName": "IotHubOverviewBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Upgrade Device Client SDK for IotHub",
  "additionalColumns": [
    {
      "name": "language",
      "title": "SDK Language"
    },
    {
      "name": "version",
      "title": "Recommended Version"
    },
    {
      "name": "deviceCount",
      "title": "Number of Impacted Devices"
    },
    {
      "name": "currentVersion",
      "title": "Current Version"
    }
  ],
  "tip": "",
  "testData": "91d12660-3dec-467a-be2a-213b5544ddc0,/subscriptions/91d12660-3dec-467a-be2a-213b5544ddc0/resourceGroups/ailn-test/providers/Microsoft.Devices/IotHubs/ailn-test,\"{\"\"language\"\":\"\"C#\"\",\"\"version\"\":\"\"1.22.0\"\",\"\"recommendedActionLearnMore\"\":\"\"https://github.com/Azure/azure-iot-sdk-csharp\"\",\"\"releaseNotes\"\":\"\"https://github.com/Azure/azure-iot-sdk-csharp/releases\"\",\"\"hubName\"\":\"\"ailn-test\"\",\"\"deviceCount\"\":\"\"12\"\",\"\"currentVersion\"\":\"\"1.12.3\"\"}\""
}
---
