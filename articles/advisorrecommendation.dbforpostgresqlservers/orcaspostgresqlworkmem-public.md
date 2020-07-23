<properties
    pageTitle="Increase the server work_mem to avoid excessive disk spilling"
    description="Increase the server work_mem to avoid excessive disk spilling"
    authors="manishku"
    ms.author="kummanish"
    articleId="2613de4e-b3d7-11e9-a2a3-2a2ae2dbcce4"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Increase the server work_mem to avoid excessive disk spilling
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "e2fa79e2-b3e0-11e9-a2a3-2a2ae2dbcce4",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlWorkMem",
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
  "learnMoreLink": "https://aka.ms/runtimeconfiguration",
  "description": "Increase the work_mem to avoid excessive disk spilling from sort and hash",
  "longDescription": "Our internal telemetry shows that the configuration work_mem is too small for your PostgreSQL server which is resulting in disk spilling and degraded query performance. To improve this, we recommend to increase the work_mem limit for the server which will help to reduce the scenarios when the sort or hash happens on disk, thereby improving the overall query performance.",
  "potentialBenefits": "Improve query performance by allocating more work_mem for the sort or hash operations thus avoiding unnecessary disk read and write.",
  "actions": [
    {
      "actionId": "d32bb2b0-b3e0-11e9-a2a3-2a2ae2dbcce4",
      "description": "Increase value of Server Parameter: work_mem",
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
      "actionId": "5d8c188f-a0de-4fb3-a27a-c30663faa9be",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Increase server parameter: work_mem",
  "additionalColumns": []
}
---
