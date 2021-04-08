<properties
    pageTitle="Upgrade to the latest Cognitive Service Text Analytics API version."
    description="Please upgrade to the latest API version for better availability and performance."
    authors="tadevteam"
    ms.author="tadevteam"
    articleId="5cb51d7e-5b86-4d49-adb5-8d4bde4afa92_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="CogSvc_TextAnalytics"
/>
# Upgrade to the latest Cognitive Service Text Analytics API version
---
{
   "recommendationOfferingId":"b31f90f9-53d3-445e-8546-5654f84ce606",
   "recommendationOfferingName":"Text Analytics",
   "$schema":"AdvisorRecommendation",
   "recommendationTypeId":"c8bbcb72-b778-48b4-882c-d8ce271995e5",
   "dataSourceMetadata":{
      "streamNamespace":"cluster('https://cogsvcff.kusto.usgovcloudapi.net').database('Platform').TAResourcesCallingOlderAPI",
      "dataSource":"Kusto",
      "refreshInterval":"12:00:00"
   },
   "recommendationCategory":"Performance",
   "recommendationImpact":"Medium",
   "recommendationResourceType":"Microsoft.CognitiveServices/accounts",
   "recommendationFriendlyName":"UpgradeToLatestAPI",
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
   "version":3.0,
   "learnMoreLink":"https://docs.microsoft.com/azure/cognitive-services/text-analytics/how-tos/text-analytics-how-to-call-api",
   "description":"Upgrade to the latest Cognitive Service Text Analytics API version",
   "longDescription":"Please upgrade to the latest API version to get the best results in terms of model quality, performance and service availability. Also there are new features are available as new endpoints starting from V3.0 such as PII recognition, Entity recognition and entity linking available as separate endpoints. In terms of changes in preview endpoints we have Opinion Mining in SA endpoint, redacted text property in PII endpoint",
   "potentialBenefits":"Better service availability and performance",
   "actions":[
      {
         "actionId":"c2094085-2f18-4a36-8eb0-6f23e6daa924",
         "description":"Upgrade to the latest Cognitive Service Text Analytics API version",
         "actionType":"Document",
         "extensionName":"",
         "bladeName":"",
         "metadata":{
         },
         "documentLink":"https://docs.microsoft.com/azure/cognitive-services/text-analytics/how-tos/text-analytics-how-to-call-api"
      }
   ],
   "resourceMetadata":{
      "action":{
         "actionId":"f1d64018-1784-469f-988f-621f5502b537",
         "actionType":"Document",
         "extensionName":"",
         "bladeName":"",
         "metadata":{
         },
         "documentLink":"https://docs.microsoft.com/azure/cognitive-services/text-analytics/how-tos/text-analytics-how-to-call-api"
      }
   },
   "displayLabel":"Upgrade to the latest Cognitive Service Text Analytics API version",
   "additionalColumns":[
   ],
   "tip":"",
   "costSavingInfo":""
}
---
