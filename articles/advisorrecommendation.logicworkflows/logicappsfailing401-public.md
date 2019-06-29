<properties
    pageTitle="Repair your log alert rule"
    description="Repair your log alert rule"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="6dcdcb36-ee1d-4507-ab15-093098330426_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Repair your log alert rule
---
{
  "recommendationOfferingId": "5818758e-7acd-4b29-834c-3af9950c477d",
  "recommendationOfferingName": "Logic Apps",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "6dcdcb36-ee1d-4507-ab15-093098330426",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('processus.kusto.windows.net').database('process').AdvisorTriggerFailure401",
    "dataSource": "Kusto",
    "refreshInterval": "00:15:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Logic/workflows",
  "recommendationFriendlyName": "LogicAppsFailing401",
  "recommendationMetadataState": "Disabled",
  "portalFeatures": [],
  "owner": {
    "email": "flowhot@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "LogicApps",
      "team": "Logic Apps Service"
    },
    "serviceTreeId": "e977b40f-c627-41e8-86c3-5fb6b5711774"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/LA-failing401",
  "description": "Resolve trigger authentication failure in Logic Apps for uninterrupted operation",
  "longDescription": "We have detected that some of your Logic Apps have a trigger that has been consistently failing due to an HTTP 401 response. This typically indicates an authentication problem where the Logic App trigger is unauthorized to access the designated API endpoint. Please ensure that the username/password or other credential value is correct.",
  "potentialBenefits": "Allow Logic App to start running by avoiding trigger failures",
  "actions": [
    {
      "actionId": "a60dd0ef-2fbc-4152-930d-eb4fa97de973",
      "description": "Review Connector Authentication",
      "actionType": "Document",
      "documentLink": "https://aka.ms/LA-failing401"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "00698e0a-891f-4518-8069-674f7126e0fb",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Resolve HTTP 401 authentication trigger failures",
  "additionalColumns": []
}
---
