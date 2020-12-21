<properties
    pageTitle="Upgrade to the latest Cognitive Service Text Analytics API version."
    description="Please upgrade to the latest API version for better availability and performance."
    authors="tadevteam"
    ms.author="tadevteam"
    articleId="8788d668-a38a-4a16-82aa-8e3da84e4ee5_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
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
      "streamNamespace":"cluster('https://cogsvc.kusto.windows.net').database('Platform').TAResourcesCallingOlderAPI",
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
         "actionId":"e1da1f35-500c-4e2b-831b-e41c68d64b56",
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
         "actionId":"87759596-22d1-48b6-8279-bb3fbb8fa720",
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
