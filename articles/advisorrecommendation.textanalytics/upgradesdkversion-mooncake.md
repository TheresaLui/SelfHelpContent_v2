<properties
    pageTitle="Upgrade to the latest SDK version."
    description="Please upgrade to the latest SDK version for better availability and performance."
    authors="tadevteam"
    ms.author="tadevteam"
    articleId="7e5a10af-0c58-400a-a212-f58e1085844c_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="CogSvc_TextAnalytics"
/>
# Upgrade to the latest SDK version
{
   "recommendationOfferingId":"b31f90f9-53d3-445e-8546-5654f84ce606",
   "recommendationOfferingName":"Text Analytics",
   "$schema":"AdvisorRecommendation",
   "recommendationTypeId":"1b94aa41-a51e-4cad-98fb-3a44447d5997",
   "dataSourceMetadata":{
      "streamNamespace":"cluster('https://cogsvcmc2.kusto.chinacloudapi.cn').database('Platform').TAResourcesWithOldSDK",
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
   "learnMoreLink":"https://docs.azure.cn/cognitive-services/text-analytics/how-tos/text-analytics-how-to-call-api",
   "description":"Upgrade to the latest SDK version",
   "longDescription":"Please upgrade to the latest SDK version for better availability and performance",
   "potentialBenefits":"Better service availability and performance",
   "supportedSDKLanguages":[
      ".Net", "Java", "Python", "JavaScript", "Ruby", "Go"
   ],
   "actions":[
      {
         "actionId":"0cc22bfa-3e93-4baa-824a-0335fd15277c",
         "description":"Steps to upgrade to the latest SDK version",
         "actionType":"Document",
         "documentLink":"{recommendedActionLearnMore}"
      },
      {
         "actionId":"4c306c22-1c9b-4a98-8838-4470e03cd7bc",
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
   "tip":""
}
---