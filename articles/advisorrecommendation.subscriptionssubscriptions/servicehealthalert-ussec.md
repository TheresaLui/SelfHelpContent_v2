<properties
    pageTitle="Create an Azure service health alert"
    description="Create an Azure service health alert"
    authors="ahex"
    ms.author="ahex"
    articleId="c6ac1f03-bd58-4421-9522-23cffb64d8e1_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USSec"
    ownershipId="CloudES_AzureResourceHealth"
/>
# Create an Azure service health alert 
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c6ac1f03-bd58-4421-9522-23cffb64d8e1",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "cluster('https://azureinsights.usseceast.kusto.core.microsoft.scloud').database('Insights').ServiceHealthAlertRecommendation",
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Low",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "ServiceHealthAlert",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "ahex@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureServiceHealth",
      "service": "Azure Service Health",
      "team": "Triage"
    },
    "serviceTreeId": "ed05f3b7-8949-4698-9b38-49ab8abb5ee0"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 3.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/service-health/alerts-activity-log-service-notifications-portal",
  "description": "Create an Azure service health alert",
  "longDescription": "Service health alerts help you stay notified when Azure service issues affect you. Create a service health alert for the regions and services that you care about.",
  "potentialBenefits": "Get notified when Azure service issues affect you",
  "actions": [
    {
      "actionId": "f8db3c62-8ed7-48ea-b313-83c7224a5c47",
      "description": "Create an Azure service health alert",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Monitoring",
      "bladeName": "CreateVNextAlertRuleBlade",
      "metadata": {
        "ruleInputs": {
          "signals": [
            {
              "subscription": "{subscriptionId}",
              "signalType": "ServiceHealth",
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
      "actionId": "da0fc147-5d91-4469-800a-3b621d41a8b2",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Create an Azure service health alert",
  "additionalColumns": [],
  "tip": "You can create a service health alert to get notified when an Azure service issue affects you."
}
---
