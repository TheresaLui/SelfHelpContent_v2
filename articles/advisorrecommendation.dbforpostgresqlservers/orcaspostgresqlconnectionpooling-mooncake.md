<properties
    pageTitle="Improve PostgreSQL connection management"
    description="Improve PostgreSQL connection management"
    authors="sunilagarwal"
    ms.author="sunila"
    articleId="84978654-5304-4b2a-81f6-022d18a8b676_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
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
    "streamNamespace": "cluster('https://sqlazurechi2.chinanorth2.kusto.chinacloudapi.cn').database('MoonCake').GetPostgreSqlConnectionPoolingRecommendations",
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
  "ingestionClientIdentities": [
    "49ebada5-bdc9-4c9b-826c-3cb789357c5d"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/azure_postgresql_connection_pooling",
  "description": "Improve PostgreSQL connection management",
  "longDescription": "Our internal telemetry indicates that your PostgreSQL server may not be managing connections efficiently. This may result in unnecessary resource consumption and overall higher application latency. To improve connection management, we recommend that you reduce the number of short-lived connections and eliminate unnecessary idle connections. This can be done by configuring a server side connection-pooler, such as PgBouncer.",
  "potentialBenefits": "Improve performance by reducing overhead associated with short-lived and idle database connections",
  "actions": [
    {
      "actionId": "04070d2f-abfd-4bbc-af66-2ddf3116ca6d",
      "description": "Configuring Connection Pooling using PgBouncer",
      "actionType": "Document",
      "documentLink": "https://aka.ms/azure_postgresql_pgbouncer"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "8ece936a-7471-4e0a-ab29-fd627098f0d6",
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
