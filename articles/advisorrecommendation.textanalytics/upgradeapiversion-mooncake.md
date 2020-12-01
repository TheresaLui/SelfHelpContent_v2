<properties
    pageTitle="Upgrade to the latest Cognitive Service Text Analytics API version."
    description="Please upgrade to the latest API version for better availability and performance."
    authors="tadevteam"
    ms.author="tadevteam"
    articleId="6edca019-750f-4b1a-afdb-726b3a0bd53c_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
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
      "streamNamespace":"cluster('https://cogsvcmc2.chinaeast2.kusto.chinacloudapi.cn').database('Platform').TAResourcesCallingOlderAPI",
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
   "learnMoreLink":"https://docs.azure.cn/cognitive-services/text-analytics/how-tos/text-analytics-how-to-call-api",
   "description":"Upgrade to the latest Cognitive Service Text Analytics API version",
   "longDescription":"Please upgrade to the latest API version to get the best results in terms of model quality, performance and service availability. Also there are new features are available as new endpoints starting from V3.0 such as PII recognition, Entity recognition and entity linking available as separate endpoints. In terms of changes in preview endpoints we have Opinion Mining in SA endpoint, redacted text property in PII endpoint",
   "potentialBenefits":"Better service availability and performance",
   "actions":[
      {
         "actionId":"acecf319-2d72-4fe1-a1bc-30795249b42b",
         "description":"Upgrade to the latest Cognitive Service Text Analytics API version",
         "actionType":"Document",
         "extensionName":"",
         "bladeName":"",
         "metadata":{
         },
         "documentLink":"https://docs.azure.cn/cognitive-services/text-analytics/how-tos/text-analytics-how-to-call-api"
      }
   ],
   "resourceMetadata":{
      "action":{
         "actionId":"0835f414-b3b8-4743-9b97-53dfd96ed370",
         "actionType":"Document",
         "extensionName":"",
         "bladeName":"",
         "metadata":{
         },
         "documentLink":"https://docs.azure.cn/cognitive-services/text-analytics/how-tos/text-analytics-how-to-call-api"
      }
   },
   "displayLabel":"Upgrade to the latest Cognitive Service Text Analytics API version",
   "additionalColumns":[
   ],
   "tip":"",
   "costSavingInfo":""
}
---
