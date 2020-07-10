<properties
    pageTitle="Right-size or shutdown underutilized virtual machines"
    description="Right-size or shutdown underutilized virtual machines"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="e10b1381-5f0a-47ff-8c7b-37bd13d7c974_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="CloudFit_CostOptimization"
/>
# Right-size or shutdown underutilized virtual machines
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "e10b1381-5f0a-47ff-8c7b-37bd13d7c974",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "LowUsageVmV2",
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
  "recommendationTimeToLive": 86400,
  "version": 6.0,
  "learnMoreLink": "https://aka.ms/aa_lowusagerec_learnmore",
  "description": "Right-size or shutdown underutilized virtual machines",
  "longDescription": "We've analyzed the usage patterns of your virtual machine over the past 7 days and identified virtual machines with low usage. While certain scenarios can result in low utilization by design, you can often save money by managing the size and number of virtual machines.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "ce37f8f7-534d-4bac-8269-74157b587a90",
      "description": "Resize {currentSku} to {targetSku}",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "size"
      },
      "condition": "targetSku != \"Shutdown\""
    },
    {
      "actionId": "1550a191-607c-4daf-ae42-8730bd77f75a",
      "description": "Shut down the virtual machine",
      "actionType": "ContextBlade",
      "extensionName": "Microsoft_Azure_CostManagement",
      "bladeName": "RecommendationDetails",
      "metadata": {
        "resource": "{resourceId}",
        "recommendation": "shutdown"
      },
      "condition": "targetSku == \"Shutdown\""
    },
    {
      "actionId": "d0fc5294-9e5a-4344-b78c-5ebc1339c399",
      "description": "View Usage Patterns",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Monitoring",
      "bladeName": "MetricsBladeV3",
      "metadata": {
        "ResourceId": "{resourceId}",
        "TimeContext": {
          "options": {
            "grain": 1
          },
          "relative": {
            "duration": 604800000
          }
        },
        "Chart": {
          "metrics": [
            {
              "resourceMetadata": {
                "id": "{resourceId}"
              },
              "name": "Percentage CPU",
              "aggregationType": 4
            }
          ]
        }
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "4d38931b-0449-4568-930e-bee998deff30",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Shut down or resize your virtual machine",
  "additionalColumns": [],
  "ingestionClientIdentities": [
    "CN=metricsclient.geneva.core.eaglex.ic.gov"
  ],
  "tip": "You can optimize underutilized virtual machines to reduce your monthly Azure spend.",
  "costSavingInfo": "*You can save up to the stated amount and your actual savings may vary."
}
---