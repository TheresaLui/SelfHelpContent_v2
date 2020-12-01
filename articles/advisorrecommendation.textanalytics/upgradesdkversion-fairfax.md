<properties
    pageTitle="Upgrade to the latest Cognitive Service Text Analytics SDK version."
    description="Please upgrade to the latest SDK version for better availability and performance."
    authors="tadevteam"
    ms.author="tadevteam"
    articleId="a52b32da-51bd-4665-9057-832e02ce396f_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	 ownershipId="CogSvc_TextAnalytics"
/>
# Upgrade to the latest Cognitive Service Text Analytics SDK version
---
{
   "recommendationOfferingId":"b31f90f9-53d3-445e-8546-5654f84ce606",
   "recommendationOfferingName":"Text Analytics",
   "$schema":"AdvisorRecommendation",
   "recommendationTypeId":"1b94aa41-a51e-4cad-98fb-3a44447d5997",
   "dataSourceMetadata":{
      "streamNamespace":"cluster('https://cogsvcff.kusto.usgovcloudapi.net').database('Platform').TAResourcesWithOldSDK",
      "dataSource":"Kusto",
      "refreshInterval":"12:00:00"
   },
   "recommendationCategory":"Performance",
   "recommendationImpact":"Medium",
   "recommendationResourceType":"Microsoft.CognitiveServices/accounts",
   "recommendationFriendlyName":"UpgradeToLatestSDK",
   "recommendationMetadataState":"Active",
   "owner":{
      "email":"tadevteam@microsoft.com",
      "icm":{
         "routingId":"mdm://adspartner/CognitiveServices/TextAnalytics",
         "service":"Cognitive Services",
         "team":"Text Analytics"
      },
      "serviceTreeId":"b31f90f9-53d3-445e-8546-5654f84ce606"
   },
   "ingestionClientIdentities":[
   ],
   "version":3,
   "learnMoreLink":"https://docs.microsoft.com/azure/cognitive-services/text-analytics/quickstarts/text-analytics-sdk?tabs=version-3-1&pivots=programming-language-csharp",
   "description":"Upgrade to the latest Cognitive Service Text Analytics SDK version",
   "longDescription":"Please upgrade to the latest SDK version for better availability and performance",
   "potentialBenefits":"Better service availability and performance",
   "supportedSDKLanguages":[
      ".Net", "Java", "Python", "JavaScript", "Ruby", "Go"
   ],
   "actions":[
      {
         "actionId":"be62660a-d6a5-49c0-a547-7096422e4910",
         "description":"Steps to upgrade to the latest Cognitive Service Text Analytics SDK version",
         "actionType":"Document",
         "documentLink":"{recommendedActionLearnMore}"
      },
      {
         "actionId":"d7c725dd-3805-4186-b0d7-7ffebd3d1bc2",
         "description":"View {version} release notes",
         "actionType":"Document",
         "documentLink":"{releaseNotes}"
      }
   ],
   "resourceMetadata":{
      "action":{
          "actionId": "091d66e1-7729-4059-bd7e-09a844a1af66",
          "description": "Check the resource",
          "actionType": "Blade",
          "extensionName": "Microsoft_CogSvc_TextAnalytics",
          "bladeName": "ResourceBlade",
          "metadata": {"id": "{resourceId}"}
      }
   },
   "displayLabel":"Upgrade to the latest SDK version for Text Analytics",
   "additionalColumns":[
      {
         "name":"language",
         "title":"SDK Language"
      },
      {
         "name":"version",
         "title":"Minimum Recommended Version"
      }
   ],
   "tip":""
}
---
