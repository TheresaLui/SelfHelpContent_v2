<properties
    pageTitle="Upgrade or mitigate deprecated Logic Apps connector"
    description="Upgrade or mitigate deprecated Logic Apps connector"
    authors="azla"
    ms.author="azla"
    articleId="d4b44636-44fc-461d-9db8-ebdb01b55d95_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="Compute_LogicApps"
/>
# Repair your log alert rule 
---
{
  "recommendationOfferingId": "5818758e-7acd-4b29-834c-3af9950c477d",
  "recommendationOfferingName": "Logic Apps",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "4440efc8-6c5c-4f65-8dea-9d0aa96790f3",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('processus.kusto.windows.net').database('process').AdvisorDeprecatedConnectors",
    "dataSource": "Kusto",
    "refreshInterval": "00:15:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Logic/workflows",
  "recommendationFriendlyName": "LogicAppsDeprecatedConnectors",
  "recommendationMetadataState": "Active",
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
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/LA-deprecatedconnectors",
  "description": "Fix deprecated connector in Logic App",
  "longDescription": "You have one or more logic apps that use a deprecated connector. Please upgrade or migrate to a newer version for more capabilities and improvements.",
  "potentialBenefits": "Newer connector versions will have more features and may improve performance.",
  "actions": [
    {
      "actionId": "3d43641e-314e-4f5b-9cb0-850c414b5673",
      "description": "Review Logic App Connectors",
      "actionType": "Document",
      "documentLink": "https://aka.ms/LA-deprecatedconnectors"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "5257ccba-b5e7-407d-942d-68cf82642c1d",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Fix deprecated connector in Logic App",
  "additionalColumns": []
}
---
