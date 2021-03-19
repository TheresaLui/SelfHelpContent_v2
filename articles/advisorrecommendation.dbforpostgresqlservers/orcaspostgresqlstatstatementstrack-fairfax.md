<properties
    pageTitle="Improve PostgreSQL performance by optimizing query statistics collection"
    description="Improve PostgreSQL performance by optimizing query statistics collection"
    authors="alau"
    ms.author="alau-ms"
    articleId="b8d89adf-9b67-4c44-8a08-5f40f5a5f1ab_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Set pg_stat_statements.track = NONE to improve PostgreSQL server performance
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "b8d89adf-9b67-4c44-8a08-5f40f5a5f1ab",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusg.kusto.usgovcloudapi.net').database('FairFax').GetPostgreSqlStatStatementsTrackRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlStatStatementsTrack",
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
  "learnMoreLink": "https://aka.ms/azure_postgresql_optimize_query_stats",
  "description": "Optimize query statistics collection on an Azure Database for PostgreSQL",
  "longDescription": "Our internal telemetry indicates that your PostgreSQL server has been configured to track query statistics using the pg_stat_statements module. While useful for troubleshooting, it can also result in reduced server performance. To improve performance, we recommend that you change the pg_stat_statements.track parameter to NONE.",
  "potentialBenefits": "Improve server performance by changing the pg_stat_statements.track parameter to NONE",
  "actions": [
    {
      "actionId": "0b335058-8b96-4063-8ebe-6779ec2ca7b2",
      "description": "Set pg_stat_statements.track to NONE",
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
      "actionId": "74d17ec4-b44a-4b25-8f75-799e460c1a0c",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Set pg_stat_statements.track to NONE",
  "additionalColumns": [],
  "tip": "You can improve your PostgreSQL server performance by changing your pg_stat_statements.track setting to NONE."
}
---