<properties
    pageTitle="Improve PostgreSQL performance by removing inactive logical replication slots"
    description="Improve PostgreSQL performance by removing inactive logical replication slots"
    authors="alau"
    ms.author="alau-ms"
    articleId="6f33a917-418c-4608-b34f-4ff0e7be8637_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Remove inactive logical replication slots to improve PostgreSQL server performance
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "6f33a917-418c-4608-b34f-4ff0e7be8637",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusg.kusto.usgovcloudapi.net').database('FairFax').GetPostgreSqlLogicalReplicationSlotsRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlLogicalReplicationSlots",
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
  "learnMoreLink": "https://aka.ms/azure_postgresql_logical_decoding",
  "description": "Improve PostgreSQL performance by removing inactive logical replication slots",
  "longDescription": "Our internal telemetry indicates that your PostgreSQL server may have inactive logical replication slots. This can result in reduced performance and server unavailability. To improve performance, we recommend that you either delete the inactive replication slots, or start using the slots so that the Log Sequence Number advances.",
  "potentialBenefits": "Improve PostgreSQL server performance by removing inactive logical replication slots",
  "actions": [
    {
      "actionId": "241f2ec5-e2e5-4f66-a11e-d7dc9226ab86",
      "description": "How to drop a logical replication slot",
      "actionType": "Document",
      "documentLink": "https://aka.ms/azure_postgresql_drop_replication_slot"
    }
  ],
  "displayLabel": "Remove inactive logical replication slots",
  "additionalColumns": [],
  "tip": "You can improve your PostgreSQL server performance by removing inactive logical replication slots."
}
---