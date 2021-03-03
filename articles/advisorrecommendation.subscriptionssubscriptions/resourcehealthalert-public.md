<properties
    pageTitle="Create an Azure Resource Health alert"
    description="Create an Azure Resource Health alert"
    authors="ahex"
    ms.author="ahex"
    articleId="c46ab673-2ddf-4a2c-927f-022616418bb0_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="CloudES_AzureResourceHealth"
/>
# Create an Azure Resource Health alert 
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c46ab673-2ddf-4a2c-927f-022616418bb0",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "cluster('https://azeeclu.kusto.windows.net').database('AzEE-DB').ResourceHealthRecommendation",
    "dataSource": "Kusto",
    "refreshInterval": "1:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Low",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "ResourceHealthAlert",
  "recommendationMetadataState": "Disabled",
  "portalFeatures": [],
  "owner": {
    "email": "ahex@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureResourceHealth",
      "service": "Azure Resource Health",
      "team": "Azure Resource Health"
    },
    "serviceTreeId": "ed05f3b7-8949-4698-9b38-49ab8abb5ee0"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 4.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/service-health/resource-health-alert-arm-template-guide",
  "description": "Create an Azure Resource Health alert",
  "longDescription": "Resource Health alerts keeps you informed about the current and historical health status of your Azure resources. Azure Resource Health alerts can notify you in near real-time when these resources have a change in their health status.",
  "potentialBenefits": "Get notified of the health of your Azure resources",
  "actions": [
    {
      "actionId": "01c7102f-e029-466c-955e-62e1c10ec8d2",
      "description": "Create an Azure Resource Health alert",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Monitoring",
      "bladeName": "CreateVNextAlertRuleBlade",
      "metadata": {
        "ruleInputs": {
          "signals": [
            {
              "subscription": "{subscriptionId}",
              "signalType": "ResourceHealth",
              "targetService": [],
              "region": [],
              "type": []
            }
          ]
        }
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "dda9461d-ffcb-4dc0-add2-b5794e18a0c1",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Create an Azure Resource Health alert",
  "additionalColumns": [],
  "testData": "e4272367-5645-4c4e-9c67-3b74b59a6982,/subscriptions/e4272367-5645-4c4e-9c67-3b74b59a6982",
  "tip": "You can create a Resource Health alert to get notified of the health status of your Azure resources."
}
---
