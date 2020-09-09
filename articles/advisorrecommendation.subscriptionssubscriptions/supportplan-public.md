<properties
    pageTitle="Upgrade to a support plan that includes technical support"
    description="Upgrade to a support plan that includes technical support"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="8189a205-7f30-4f97-90ab-230519248722_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="CloudES_AzureSupportCenter"
/>
# Upgrade to a support plan that includes technical support
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "8189a205-7f30-4f97-90ab-230519248722",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "AzureAdvisor.SupportPlan",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "SupportPlan",
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
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/azuresupport",
  "description": "Upgrade to a support plan that includes technical support",
  "longDescription": "We recommend upgrading your support plan to include technical support. Explore the range of Azure support options and choose the plan that best fits, whether you're a developer just starting your cloud journey or a large organization deploying business-critical, strategic applications.",
  "potentialBenefits": "Ensure business continuity by having access to Azure cloud experts",
  "actions": [
    {
      "actionId": "aa92b605-0e5b-4801-99f9-65ee7a8e29f8",
      "description": "Upgrade your support plan",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Support",
      "bladeName": "SupportPlansBlade",
      "metadata": {
        "subscriptionId": "{subscriptionId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "95915159-a170-46aa-b4dd-1709543ab5df",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Upgrade your support plan",
  "additionalColumns": [],
  "tip": "You can upgrade your support plan to include technical support."
}
---
