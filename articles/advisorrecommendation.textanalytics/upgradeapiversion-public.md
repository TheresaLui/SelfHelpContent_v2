# Upgrade to the latest API version
---
{
   "recommendationOfferingId":"b31f90f9-53d3-445e-8546-5654f84ce606",
   "recommendationOfferingName":"Text Analytics",
   "$schema":"AdvisorRecommendation",
   "recommendationTypeId":"c8bbcb72-b778-48b4-882c-d8ce271995e5",
   "dataSourceMetadata":{
      "streamNamespace":"cluster('https://cogsvc.kusto.windows.net').database('Platform').TAResourcesCallingOlderAPI",
      "dataSource":"Kusto",
      "refreshInterval":"1.00:00:00"
   },
   "recommendationCategory":"Performance",
   "recommendationImpact":"High",
   "recommendationResourceType":"Microsoft.CognitiveServices/accounts",
   "recommendationFriendlyName":"UpgradeToLatestAPI",
   "recommendationMetadataState":"Active",
   "owner":{
      "email":"tadevteam@microsoft.com",
      "icm":{
         "routingId":"icmportal://routing/85633E54D0D64D46A2F9F5DEC68E204C",
         "service":"Cognitive Services",
         "team":"Text Analytics"
      },
      "serviceTreeId":"b31f90f9-53d3-445e-8546-5654f84ce606"
   },
   "ingestionClientIdentities":[
   ],
   "version":1.0,
   "learnMoreLink":"https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/how-tos/text-analytics-how-to-call-api",
   "description":"Upgrade to the latest API version",
   "longDescription":"Please upgrade to the latest API version for better availability and performance",
   "potentialBenefits":"Better service availability and performance",
   "actions":[
      {
         "actionId":"e1da1f35-500c-4e2b-831b-e41c68d64b56",
         "description":"Upgrade to latest API version",
         "actionType":"Document",
         "extensionName":"",
         "bladeName":"",
         "metadata":{
         },
         "documentLink":"https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/how-tos/text-analytics-how-to-call-api"
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
         "documentLink":"https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/how-tos/text-analytics-how-to-call-api"
      }
   },
   "displayLabel":"Upgrade to the latest API version",
   "additionalColumns":[
   ],
   "tip":"",
   "costSavingInfo":"",
   "testData":""
}
---