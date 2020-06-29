<properties
          pageTitle="Upgrade to the latest SDK version"
          description ="Send a recommendation that the user should upgrade their SDK version to the most recent major version."
          authors="adsandor"
          ms.author="cplatsdkdev"
          articleId="158f0a07-0a66-4a25-9e37-c43c49c8dd64_Public"
          selfHelpType="advisorRecommendationMetadata"
          cloudEnvironments="Public"
          ownershipId="Compute_ComputePlatform"
/>

# Recommend upgrading to a more recent SDK API version.
---
{"recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
"recommendationOfferingName": "Virtual Machines",
"$schema": "AdvisorRecommendation",
"recommendationTypeId": "158f0a07-0a66-4a25-9e37-c43c49c8dd64",
"recommendationCategory": "Performance",
"recommendationImpact": "High",
"recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
"recommendationFriendlyName": "UpgradeSDKVersion",
"recommendationMetadataState": "Active",
"owner":
  { "email": "cplatsdkdev@microsoft.com",
          "icm": { "routingId": "mdm:/adspartner/AzureRTCPlatSDK/Powershell",
                  "service": "AzureRT",
                  "team": "CPlat SDK/PowerShell"
                  },
         "serviceTreeId": "ae53b53f-9347-4198-b9b7-ff4b8228d6a7"
  },
  "version": 1.0,
  "learnMoreLink": "https://github.com/Azure/azure-sdk/blob/master/README.md#azure-sdk",
  "description": "Upgrade to the recommended SDK version to ensure you avoid performance issues.",
  "longDescription": "You have recently invoked an SDK version that is significantly out of date. The old SDK can lead to the utilization of processes that later versions improved. If many SDK versions are out of date, the inefficient processes can compound and lead to significant problems. Regularly updating to more recent SDK versions will help prevent this.",
  "potentialBenefits": "Ensure business continuity through API improvements.",
  "displayLabel": "Upgrade SDK Vesion",
  "tip": "Upgrade to the recommended SDK version to ensure you avoid performance issues.",
  "supportedSDKLanguages": [".Net", "Java", "JavaScript", "Python"],
  "actions": [{
                    "actionId": "0a71357b-bf25-439e-8e69-6bc1538279ae",
                    "description": "Upgrade to the recommended SDK version.",
                    "actionType": "Document",
                    "documentLink": "https://github.com/Azure/azure-sdk/blob/master/README.md"
          }],
  "dataSourceMetadata":
          {
                    "streamNamespace": "cluster('https://cplatsdk.westus2.kusto.windows.net').database('sdk').StaleSDKRecommendation",
                    "dataSource": "Kusto",
                    "refreshInterval": "0.00:05:00"
          }
}
---
