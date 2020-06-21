<properties
    pageTitle="Follow App Service Advisor recommendations"
    description="Follow App Service Advisor recommendations"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="85650d10-4245-40f6-a3e5-db1e70728a47_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="Compute_AppService"
/>
# Follow App Service Advisor recommendations
---
{
  "recommendationOfferingId": "c7f69506-5b4f-4751-b423-0095e68fad64",
  "recommendationOfferingName": "App Service",
  "$schema": "AdvisorRecommendation",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationTypeId": "85650d10-4245-40f6-a3e5-db1e70728a47",
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Web/sites",
  "recommendationFriendlyName": "AppServicePerf",
  "recommendationMetadataState": "Disabled",
  "portalFeatures": [],
  "owner": {
    "email": "aadevteam@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Azure Advisor",
      "team": "Azure Advisor"
    },
    "serviceTreeId": "f6d7f416-ee14-4943-894b-1abca9140b74"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/appservicerec_learnmore",
  "description": "Follow App Service Advisor recommendations",
  "longDescription": "Follow the recommendations from App Service Advisor.",
  "potentialBenefits": "Improved reliability and performance",
  "actions": [
    {
      "actionId": "8e1bee12-a724-4724-b414-1be72c7fb12f",
      "actionType": "Document",
      "description": "Follow the recommendations from App Service Advisor.",
      "documentLink": "https://aka.ms/appservicerec_learnmore"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "5776a411-0804-4f1c-a4d5-cbca569db79b",
      "actionType": "Blade",
      "extensionName": "WebsitesExtension",
      "bladeName": "WebsiteBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "App Service Advisor Recommendations",
  "additionalColumns": [],
  "onDemand": true,
  "legacyRecommender": {
    "className": "Microsoft.Azure.Advisor.Common.Recommenders.AppServiceRecommender",
    "assemblyName": "Microsoft.Azure.Advisor.Common"
  },
  "tip": "You can improve the performance of your App Services instances."
}
---
