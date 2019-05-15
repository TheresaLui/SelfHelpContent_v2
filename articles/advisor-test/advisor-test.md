<properties
    pageTitle="Create an Azure service health alert"
    description="Create an Azure service health alert"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="c6ac1f03-bd58-4421-9522-23cffb64d8e1_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Create an Azure service health alert
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c6ac1f03-bd58-4421-9522-23cffb64d8e1",
  "dataSourceMetadata": {
    "streamNamespace": "AzureAdvisor.ServiceHealthAlert_Large",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Low",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "ServiceHealthAlert",
  "recommendationMetadataState": "Active",
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
  "learnMoreLink": "https://aka.ms/aa_servicehealthalert_action",
  "description": "Create an Azure service health alert",
  "longDescription": "Service health alerts help you stay notified when Azure service issues affect you. Create a service health alert for the regions and services that you care about.",
  "potentialBenefits": "Get notified when Azure service issues affect you",
  "actions": [
    {
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
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Create an Azure service health alert",
  "testData": "658c8950-e79d-4704-a903-1df66ba90258,/subscriptions/658c8950-e79d-4704-a903-1df66ba90258",
  "additionalColumns": []
}
---
