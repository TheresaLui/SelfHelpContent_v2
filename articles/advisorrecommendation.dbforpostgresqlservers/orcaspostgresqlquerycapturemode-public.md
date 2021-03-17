<properties
    pageTitle="Improve PostgreSQL performance by optimizing query store settings"
    description="Improve PostgreSQL performance by optimizing query store settings"
    authors="alau"
    ms.author="alau-ms"
    articleId="feba5625-68c8-4b53-90b4-8a9de4f71e9e_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Set pg_qs.query_capture_mode = NONE to improve PostgreSQL server performance
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "feba5625-68c8-4b53-90b4-8a9de4f71e9e",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlQueryCaptureMode",
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
  "learnMoreLink": "https://aka.ms/azure_postgresql_query_store",
  "description": "Optimize query store on an Azure Database for PostgreSQL",
  "longDescription": "Our internal telemetry indicates that your PostgreSQL server has been configured to track query performance using the pg_qs.query_capture_mode parameter. While useful for troubleshooting, it can also result in reduced server performance. To improve performance, we recommend that you change the pg_qs.query_capture_mode parameter to NONE.",
  "potentialBenefits": "Improve server performance by changing the pg_qs.query_capture_mode parameter to NONE",
  "actions": [
    {
      "actionId": "66bace85-28c0-41c0-b2a7-1b6c343d0400",
      "description": "Set pg_qs.query_capture_mode to NONE",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "PostgreSqlServerParametersBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "807f6c27-1491-4b15-9dbb-6d99dc27379d",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Set pg_qs.query_capture_mode to NONE",
  "additionalColumns": [],
  "tip": "You can improve your PostgreSQL server performance by changing your pg_qs.query_capture_mode setting to NONE."
}
---