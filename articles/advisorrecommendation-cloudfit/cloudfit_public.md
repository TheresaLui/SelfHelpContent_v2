<properties
    pageTitle="e10b1381-5f0a-47ff-8c7b-37bd13d7c974_Public"
    description="e10b1381-5f0a-47ff-8c7b-37bd13d7c974_Public"
    authors="aadevteam"
    ms.author"aadevteam"
    articleId="e10b1381-5f0a-47ff-8c7b-37bd13d7c974_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# e10b1381-5f0a-47ff-8c7b-37bd13d7c974_Public
---
{
  "recommendationTypeId": "e10b1381-5f0a-47ff-8c7b-37bd13d7c974",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "category": "Cost",
  "impact": "High",
  "resourceType": "Microsoft.Compute/virtualMachines",
  "friendlyName": "LowUsageVmV2",
  "state": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "aadevteam@microsoft.com",
    "IcM": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Azure Advisor",
      "team": "Azure Advisor"
    },
    "serviceTreeId": "f6d7f416-ee14-4943-894b-1abca9140b74"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 5.0,
  "description": "Right-size or shutdown underutilized virtual machines",
  "longDescription": "We've analyzed the usage patterns of your virtual machine over the past 7 days and identified virtual machines with low usage. While certain scenarios can result in low utilization by design, you can often save money by managing the size and number of virtual machines.",
  "potentialBenefits": "savings",
  "learnMoreLink": "https://aka.ms/aa_lowusagerec_learnmore",
  "actions": [
    {
      "description": "Resize the virtual machine",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "size"
      }
    },
    {
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
    },
    {
      "description": "Shut down the virtual machine",
      "actionType": "ContextBlade",
      "extensionName": "Microsoft_Azure_CostManagement",
      "bladeName": "RecommendationDetails",
      "metadata": {
        "resource": "{resourceId}",
        "recommendation": "shutdown"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "description": "{vmSize} virtual machines in {location}",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Shut down or resize your virtual machine",
  "tip": "You can optimize underutilized virtual machines to reduce your monthly Azure spend.",
  "costSavingInfo": "*You can save up to the stated amount if you choose to shut down the virtual machine. Your actual savings may vary.",
  "additionalColumns": [
    {
      "name": "targetResourceCount",
      "title": "Recommended Quantity"
    }
  ]
}
---
