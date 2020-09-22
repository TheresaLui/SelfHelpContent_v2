<properties
    pageTitle="Increase the reliability of audit logs"
    description="Increase the reliability of audit logs"
    authors="ambhatna"
    ms.author="ambhatna"
    articleId="a77dd319-ffb5-4f88-bdf2-e98e59afc79f_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="ussec"
    ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Increase the reliability of audit logs 
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a77dd319-ffb5-4f88-bdf2-e98e59afc79f",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureussece.usseceast.kusto.core.microsoft.scloud').database('sqlazure1').GetMariaDbAuditLogRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForMariadb/servers",
  "recommendationFriendlyName": "OrcasMariaDBAuditLog",
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
  "learnMoreLink": "https://aka.ms/mariadb-audit-logs",
  "description": "Increase the reliability of audit logs",
  "longDescription": "Our internal telemetry shows that the server's audit logs may have been lost over the past day. This can occur when your server is experiencing a CPU heavy workload or a server generates a large number of audit logs over a short period of time. We recommend only logging the necessary events required for your audit purposes using the following server parameters: audit_log_events, audit_log_exclude_users, audit_log_include_users. If the CPU usage on your server is high due to your workload, we recommend increasing the server's vCores to improve performance.",
  "potentialBenefits": "Improve the reliability of audit logs for monitoring and troubleshooting.",
  "actions": [
    {
      "actionId": "8c9860b1-0c87-4308-be82-e808f7777d17",
      "description": "Update your audit log settings.",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "MariaDBServerParametersBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    },
    {
        "actionId": "cb9848dc-595f-4928-abf1-9222d1979237",
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
      "actionId": "175e721d-b9c8-4033-ad8b-b392bcdb4e7f",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Increase the reliability of MariaDB audit logs.",
  "additionalColumns": [],
  "tip": "You can improve the reliability of MariaDB audit logs by only logging events you need."
}
---
