<properties
    pageTitle="Increase the reliability of audit logs"
    description="Increase the reliability of audit logs"
    authors="andrela"
    ms.author="ajlam"
    articleId="a77dd319-ffb5-4f88-bdf2-e98e59afc79f_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
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
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').GetMariaDbAuditLogRecommendations",
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
      "actionId": "c1cb1fbf-8fe9-4ef3-bf11-d852bcdac641",
      "description": "Update your audit log settings.",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "MariaDBServerParametersBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    },
    {
        "actionId": "de27d1dd-3e67-4ca8-8431-9fa9bcf06d92",
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
      "actionId": "27d66d9c-7e0a-484f-b40b-0282b7d8d619",
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
