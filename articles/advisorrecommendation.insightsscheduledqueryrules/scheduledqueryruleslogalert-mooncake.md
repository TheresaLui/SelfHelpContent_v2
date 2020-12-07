<properties
    pageTitle="Repair your log alert rule"
    description="Repair your log alert rule"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="2b5eac39-9f50-4d8d-bc9b-1e1e07c5c37e_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>
# Repair your log alert rule Mooncake
---
{
  "recommendationOfferingId": "ee5716b5-e6fd-480a-9396-0343b023dfa5",
  "recommendationOfferingName": "Azure Monitor",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "2b5eac39-9f50-4d8d-bc9b-1e1e07c5c37e",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://almonprodmc.chinaeast2.kusto.chinacloudapi.cn').database('LogSearchRule').AdvisorRecommendations",
    "dataSource": "Kusto",
    "refreshInterval": "08:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Insights/ScheduledQueryRules",
  "recommendationFriendlyName": "ScheduledQueryRulesLogAlert",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "lsateam@microsoft.com",
    "icm": {
      "routingId": "AIMS://LogAlertsFlow",
      "service": "Azure Log Search Alerts",
      "team": "Log Search Alerts (Scheduled Query Rules) On Call"
    },
    "serviceTreeId": "6b503797-6dcf-4f37-861f-a76db539a823"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/aa_logalerts_queryrepair",
  "description": "Repair your log alert rule",
  "longDescription": "We have detected that one or more of your alert rules have invalid queries specified in their condition section. Log alert rules are created in Azure Monitor and are used to run analytics queries at specified intervals. The results of the query determine if an alert needs to be triggered. Analytics queries may become invalid overtime due to changes in referenced resources, tables, or commands. We recommend that you correct the query in the alert rule to prevent it from getting auto-disabled and ensure monitoring coverage of your resources in Azure.",
  "potentialBenefits": "Ensure continued monitoring and alerting for your resources",
  "actions": [
    {
      "actionId": "2cd24f57-8293-438c-a5e5-674c2f6ca560",
      "description": "Repair your log alert rule to ensure monitoring",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Monitoring",
      "bladeName": "UpdateVNextAlertRuleBlade",
      "metadata": {
        "ruleInputs": {
          "alertId": "{resourceId}"
        }
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "48c2161c-794c-423e-b049-ca2098fed0bf",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Monitoring",
      "bladeName": "UpdateVNextAlertRuleBlade",
      "metadata": {
        "ruleInputs": {
          "alertId": "{resourceId}"
        }
      }
    }
  },
  "displayLabel": "Repair log alert rule",
  "additionalColumns": []
}
---
