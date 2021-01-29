<properties
    pageTitle="Increase the reliability of audit logs"
    description="Increase the reliability of audit logs"
    authors="ambhatna"
    ms.author="ambhatna"
    articleId="997839f4-48e4-49e4-9b15-628a7757765c_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
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
    "streamNamespace": "cluster('https://sqlazurechi2.chinanorth2.kusto.chinacloudapi.cn').database('MoonCake').GetMySqlAuditLogRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
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
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/mysql-audit-logs",
  "description": "Increase the reliability of audit logs",
  "longDescription": "Our internal telemetry shows that the server's audit logs may have been lost over the past day. This can occur when your server is experiencing a CPU heavy workload or a server generates a large number of audit logs over a short period of time. We recommend only logging the necessary events required for your audit purposes using the following server parameters: audit_log_events, audit_log_exclude_users, audit_log_include_users. If the CPU usage on your server is high due to your workload, we recommend increasing the server's vCores to improve performance.",
  "potentialBenefits": "Improve the reliability of audit logs for monitoring and troubleshooting.",
  "actions": [
    {
      "actionId": "5a18a765-2968-4ff4-bb8d-9f7972cd31f2",
      "description": "Update your audit log settings.",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "MySqlServerParametersBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    },
    {
        "actionId": "c9562c4b-9bd1-45b6-8d63-08e05d97f1c9",
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
      "actionId": "6e4081b4-78da-4a89-a9b9-42c89612fd4d",
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