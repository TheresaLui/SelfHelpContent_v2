# Upgrade to the latest SDK version
{
   "recommendationOfferingId":"b31f90f9-53d3-445e-8546-5654f84ce606",
   "recommendationOfferingName":"Text Analytics",
   "$schema":"AdvisorRecommendation",
   "recommendationTypeId":"790f5b30-ee0d-4b1c-9212-eff623a1aa46",
   "dataSourceMetadata":{
      "streamNamespace":"cluster('https://cogsvcff.kusto.usgovcloudapi.net').database('Platform').TAResourcesWithOldSDK",
      "dataSource":"Kusto",
      "refreshInterval":"1.00:00:00"
   },
   "recommendationCategory":"Performance",
   "recommendationImpact":"High",
   "recommendationResourceType":"Microsoft.CognitiveServices/accounts",
   "recommendationFriendlyName":"UpgradeToLatestSDK",
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
   "version":1,
   "learnMoreLink":"https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/quickstarts/text-analytics-sdk?tabs=version-3-1&pivots=programming-language-csharp",
   "description":"Upgrade to the latest SDK version",
   "longDescription":"Please upgrade to the latest SDK version for better availability and performance",
   "potentialBenefits":"Better service availability and performance",
   "supportedSDKLanguages":[
      ".Net", "Java", "Python", "JavaScript", "Ruby", "Go"
   ],
   "actions":[
      {
         "actionId":"be62660a-d6a5-49c0-a547-7096422e4910",
         "description":"Steps to upgrade to the latest SDK version",
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
         "actionId":"",
         "actionType":"",
         "extensionName":"",
         "bladeName":"",
         "metadata":{
         },
         "documentLink":""
      }
   },
   "displayLabel":"",
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
   "tip":"",
   "testData":""
}
---