<properties
          pageTitle="Upgrade to the latest SDK version"
          description ="Send a recommendation that the user should update their SDK version to the most recent major version."
          authors="adsandor"
          ms.author="cplatsdkdev"
          articleId=""
          selfHelpType="advisorRecommendationMetadata"
          cloudEnvironments="Public"
          ownershipId=""
/>

# Recommend upgrading to a more recent SDK API version.
---
{ 
"recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
"recommendationOfferingName": "Virtual Machines",
"$schema": "AdvisorRecommendation",
"recommendationTypeId": "",
"recommendationCategory": "Performance", 
"recommendationImpact": "High",
"recommendationResourceType": "",
"recommendationFriendlyName": "UpgradeSDKVersion",
"recommendationMetadataState": "Active",
"owner": 
  { "email": "cplatsdkdev@microsoft.com", 
          "icm": { "routingId": "",
                  "service": "AzureRT",
                  "team": "CPlat SDK/PowerShell"
                  },
         "serviceTreeId": "92a514eb-a2bc-48e3-a6f2-262f18a2ce40"
  },
  "version": 1.0,
  "learnMoreLink": "https://github.com/Azure/azure-sdk/blob/master/README.md",
  "description": "Upgrade to the recommended SDK version to ensure you avoid performance issues.",
  "longDescription": "You have recently invoked an SDK version that is significantly out of date. The old SDK can lead to the utilization of processes that later versions improved. If many SDK versions are out of date, the inefficient processes can compound and lead to significant problems. Regularly updating to more recent SDK versions will help prevent this.",
  "potentialBenefits": "Ensure business continuity through API improvements.",
  "displayLabel": "Update SDK Vesion",
  "additionalColumns": {"name": "staleSDKRecommendation", "title": "Update SDK Version"},
  "tip": "Upgrade to the recommended SDK version to ensure you avoid performance issues.",
  "supportedSDKLanguages": [".Net", "Java", "JavaScript", "Python"], 
  "actions": [{
                    "actionId": "",
                    "description": "Upgrade to the recommended SDK version.",
                    "actionType": "Document",
                    "condition": "",
                    "documentLink": "https://github.com/Azure/azure-sdk/blob/master/README.md"
          }],
  "dataSourceMetadata": 
          {
                    "streamNamespace": "cluster('https://cplatsdk.westus2.kusto.windows.net').database('sdk').StaleSDKRecommendation", 
                    "dataSource": "Kusto",
                    "refreshInterval": "1.00:00:00"
          }
}
