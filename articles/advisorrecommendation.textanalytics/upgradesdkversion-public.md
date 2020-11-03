# Upgrade to the latest SDK version
{
   "recommendationOfferingId":"b31f90f9-53d3-445e-8546-5654f84ce606",
   "recommendationOfferingName":"Text Analytics",
   "$schema":"AdvisorRecommendation",
   "recommendationTypeId":"1b94aa41-a51e-4cad-98fb-3a44447d5997",
   "dataSourceMetadata":{
      "streamNamespace":"cluster('https://cogsvc.kusto.windows.net').database('Platform').TAResourcesWithOldSDK",
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
         "actionId":"55b6a59e-135d-4111-99ae-f46c70b584ab",
         "description":"Steps to upgrade to the latest SDK version",
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