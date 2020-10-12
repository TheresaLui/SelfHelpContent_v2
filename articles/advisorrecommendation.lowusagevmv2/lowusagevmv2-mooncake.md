<properties
    pageTitle="Right-size or shutdown underutilized virtual machines"
    description="Right-size or shutdown underutilized virtual machines"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="e10b1381-5f0a-47ff-8c7b-37bd13d7c974_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
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
  "version": 5.0,
  "learnMoreLink": "https://aka.ms/aa_lowusagerec_learnmore_cn",
  "description": "Right-size or shutdown underutilized virtual machines",
  "longDescription": "We've analyzed the usage patterns of your virtual machine over the past 7 days and identified virtual machines with low usage. While certain scenarios can result in low utilization by design, you can often save money by managing the size and number of virtual machines.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "09d5e15f-f683-4e29-bca1-869440219457",
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
      "actionId": "a0255f1a-6f92-489a-8547-4ec5162e31a6",
      "description": "Shut down the virtual machine",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      },
      "condition": "targetSku == \"Shutdown\""
    },
    {
      "actionId": "50a927a5-3a86-4605-b083-a5aea4beb273",
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
      "actionId": "f4ef149e-dab9-487f-be20-85d4f32cd599",
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
    "CN=metricsclient.geneva.core.windows.net;CN=Microsoft IT TLS CA 1, OU=Microsoft IT, O=Microsoft Corporation, L=Redmond, S=Washington, C=US"
  ],
  "tip": "You can optimize underutilized virtual machines to reduce your monthly Azure spend.",
  "costSavingInfo": "*You can save up to the stated amount and your actual savings may vary."
}
---
