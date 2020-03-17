<properties
    pageTitle="Add a PostgreSQL Read Replica server"
    description="Add a PostgreSQL Read Replica server"
    authors="manishku"
    ms.author="kummanish"
    articleId="8fd46c9b-5ba1-4133-8a5d-dfc61e1195b1_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Add a PostgreSQL Read Replica server
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "8fd46c9b-5ba1-4133-8a5d-dfc61e1195b1",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusg.kusto.usgovcloudapi.net').database('FairFax').GetPostgreSqlReadReplicaRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlReadReplica",
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
  "learnMoreLink": "https://aka.ms/postgresqlreadreplica",
  "description": "Add a PostgreSQL Read Replica server",
  "longDescription": "Our internal telemetry shows that you may have a read intensive workload running, which results in resource contention for this server. This may lead to slow query performance for the server. To improve performance, we recommend you add a read replica, and offload some of your read workloads to the replica.",
  "potentialBenefits": "Improve query performance by scaling out reads",
  "actions": [
    {
      "actionId": "eea28ada-6362-4597-9872-7855e354fc14",
      "description": "Scale out your read workload by adding a replica",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "PostgreSqlServerReplicationBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "447a0a3f-c23c-4d03-aa82-7409e668fdef",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Add PostgreSQL Read Replica",
  "additionalColumns": [],
  "tip": "You can improve the query performance of your PostgreSQL database my adding a Read Replica server."
}
---
