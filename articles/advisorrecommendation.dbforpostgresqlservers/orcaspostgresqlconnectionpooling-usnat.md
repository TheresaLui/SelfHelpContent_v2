<properties
    pageTitle="Improve PostgreSQL connection management"
    description="Improve PostgreSQL connection management"
    authors="alau"
    ms.author="alau"
    articleId="84978654-5304-4b2a-81f6-022d18a8b676_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="usnat"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Improve PostgreSQL connection management
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "84978654-5304-4b2a-81f6-022d18a8b676",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').GetPostgreSqlConnectionPoolingRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForPostgreSql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlConnectionPooling",
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
  "learnMoreLink": "https://aka.ms/azure_postgresql_connection_pooling",
  "description": "Improve PostgreSQL connection management",
  "longDescription": "Our internal telemetry indicates that your PostgreSQL server may not be managing connections efficiently. This may result in unnecessary resource consumption and overall higher application latency. To improve connection management, we recommend that you reduce the number of short-lived connections and eliminate unnecessary idle connections. This can be done by configuring a server side connection-pooler, such as PgBouncer.",
  "potentialBenefits": "Improve performance by reducing overhead associated with short-lived and idle database connections",
  "actions": [
    {
      "actionId": "c567d562-4e11-48bd-adff-8d942738dc92",
      "description": "Configuring Connection Pooling using PgBouncer",
      "actionType": "Document",
      "documentLink": "https://aka.ms/azure_postgresql_pgbouncer"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "3f0c2945-45d9-4742-9a7d-805b52c164fe",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Improve PostgreSQL connection management",
  "additionalColumns": [],
  "tip": "You can manage your PostgreSQL database connections more efficiently by configuring a connection pooler, such as PgBouncer."
}
---
