<properties
    pageTitle="Upgrade to the latest Cognitive Service Text Analytics SDK version."
    description="Please upgrade to the latest SDK version for better availability and performance."
    authors="tadevteam"
    ms.author="tadevteam"
    articleId="09f490d5-625a-44ca-8089-58947548ead8_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
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
      "streamNamespace":"cluster('https://cogsvc.kusto.windows.net').database('Platform').TAResourcesWithOldSDK",
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
   "longDescription":"Please upgrade to the latest SDK version to get the best results in terms of model quality, performance and service availability. Also there are new features are available as new endpoints starting from V3.0 such as PII recognition, Entity recognition and entity linking available as separate endpoints. In terms of changes in preview endpoints we have Opinion Mining in SA endpoint, redacted text property in PII endpoint",
   "potentialBenefits":"Better service availability and performance",
   "supportedSDKLanguages":[
      ".Net", "Java", "Python", "JavaScript", "Ruby", "Go"
   ],
   "actions":[
      {
         "actionId":"55b6a59e-135d-4111-99ae-f46c70b584ab",
         "description":"Steps to upgrade to the latest Cognitive Service Text Analytics SDK version",
         "actionType":"Document",
         "documentLink":"{recommendedActionLearnMore}"
      },
      {
         "actionId":"82e3811b-f879-4d7f-af41-0a3bbb1431d7",
         "description":"View {version} release notes",
         "actionType":"Document",
         "documentLink":"{releaseNotes}"
      }
   ],
   "resourceMetadata":{
      "action":{
         "actionId": "17fe3545-7057-47ab-bf65-83f63516c290",
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
