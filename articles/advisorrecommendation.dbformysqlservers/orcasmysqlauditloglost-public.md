<properties
    pageTitle="Increase the reliability of audit logs"
    description="Increase the reliability of audit logs"
    authors="andrela"
    ms.author="ajlam"
    articleId="997839f4-48e4-49e4-9b15-628a7757765c_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Increase the reliability of audit logs
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "997839f4-48e4-49e4-9b15-628a7757765c",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForMysql/servers",
  "recommendationFriendlyName": "OrcasMySQLAuditLog",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "orcasql-livesite@service.microsoft.com",
    "icm": {
      "routingId": "AIMS://AZURE OSS DATABASES/Open Source RDBMS",
      "service": "Azure OSS Databases",
      "team": "Open Source RDBMS (Project OrcaSQL)"
    },
    "serviceTreeId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a"
  },
  "ingestionClientIdentities": [
    "49ebada5-bdc9-4c9b-826c-3cb789357c5d"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/mysql-audit-logs",
  "description": "Increase the reliability of audit logs",
  "longDescription": "Our internal telemetry shows that the server's audit logs may have been lost over the past day. This can occur when your server is experiencing a CPU heavy workload or a server generates a large number of audit logs over a short period of time. We recommend only logging the necessary events required for your audit purposes using the following server parameters: audit_log_events, audit_log_exclude_users, audit_log_include_users. If the CPU usage on your server is high due to your workload, we recommend increasing the server's vCores to improve performance.",
  "potentialBenefits": "Improve the reliability of audit logs for monitoring and troubleshooting.",
  "actions": [
    {
      "actionId": "a6c2cd8a-bd92-4aa1-bb9c-fc7ac4db3a94",
      "description": "Update your audit log settings.",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "MySqlServerParametersBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    },
    {
        "actionId": "e18e24de-462f-48f6-808a-0e405dd39af8",
        "description": "Increase vCores",
        "actionType": "Blade",
        "extensionName": "HubsExtension",
        "bladeName": "ResourceMenuBlade",
        "metadata": {
        "id": "{resourceId}",
        "menuid": "pricingTier"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "218893cf-794b-4e61-813a-e2065ad148fd",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Increase the reliability of MySQL audit logs.",
  "additionalColumns": [],
  "tip": "You can improve the reliability of MySQL audit logs by only logging events you need."
}
---
