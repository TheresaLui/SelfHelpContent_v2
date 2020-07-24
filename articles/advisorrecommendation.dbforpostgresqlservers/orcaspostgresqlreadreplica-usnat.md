<properties
    pageTitle="Add a PostgreSQL Read Replica server"
    description="Add a PostgreSQL Read Replica server"
    authors="manishku"
    ms.author="kummanish"
    articleId="8fd46c9b-5ba1-4133-8a5d-dfc61e1195b1_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="usnat"
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
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').GetPostgreSqlReadReplicaRecommendations",
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
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/postgresqlreadreplica",
  "description": "Add a PostgreSQL Read Replica server",
  "longDescription": "Our internal telemetry shows that you may have a read intensive workload running, which results in resource contention for this server. This may lead to slow query performance for the server. To improve performance, we recommend you add a read replica, and offload some of your read workloads to the replica.",
  "potentialBenefits": "Improve query performance by scaling out reads",
  "actions": [
    {
      "actionId": "0a61b612-fe86-4485-8398-4a8e5a3ad43e",
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
      "actionId": "9a76b5cb-e764-4fe0-8d52-fd56d8fd4e48",
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
