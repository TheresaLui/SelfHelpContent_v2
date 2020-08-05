<properties
          pageTitle="Upgrade to the latest SDK version"
          description ="Update your current SDK version to the most recent version."
          authors="adsandor"
          ms.author="cplatsdkdev"
          articleId="158f0a07-0a66-4a25-9e37-c43c49c8dd64_Public"
          selfHelpType="advisorRecommendationMetadata"
          cloudEnvironments="Public, ussec, usnat"
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
"recommendationFriendlyName": "ComputeStaleSDKRecommendation",
"recommendationMetadataState": "Active",
"owner":
  { "email": "cplatsdkdev@microsoft.com",
          "icm": { "routingId": "mdm:/adspartner/AzureRTCPlatSDK/Powershell",
                  "service": "AzureRT",
                  "team": "CPlat SDK/PowerShell"
                  },
         "serviceTreeId": "ae53b53f-9347-4198-b9b7-ff4b8228d6a7"
  },
  "version": 4.0,
  "learnMoreLink": "https://aka.ms/azureSDKReadMe",
  "description": "Update your current Compute Management SDK version to the most recent version.",
  "longDescription": "We have identified operations under this subscription using outdated Compute Management SDK versions. We recommend switching to the latest Compute Management SDK versions, which might involve changes to your existing codebase, to obtain improved security and performance.",
  "potentialBenefits": "Improved security, performance, data resiliency, and support for new features.",
  "displayLabel": "Update your current Compute Management SDK version to the most recent version",
  "tip": "Regularly update your Compute Management SDK versions to prevent security issues and access new features.",
  "supportedSDKLanguages": [".Net", "Java", "JavaScript", "Python"],
  "actions": [{
                    "actionId": "0a71357b-bf25-439e-8e69-6bc1538279ae",
                    "description": "Upgrade your current {language} SDK to the latest version, {version}",
                    "actionType": "Document",
                    "documentLink": "{recommendedActionLearnMore}"
          },
          {
                    "actionId": "11941fbb-2321-4a49-a34d-25c007404331",
                    "description": "Learn more about the latest {language} SDK version, {version}",
                    "actionType": "Document",
                    "documentLink": "{releaseNotes}"
          }],
  "dataSourceMetadata":
          {
                    "streamNamespace": "cluster('https://advisorfollower.centralus.kusto.windows.net').database('ARMProdHelper').StaleSDKRecommendation",
                    "dataSource": "Kusto",
                    "refreshInterval": "0.02:00:00"
          }
}
---
