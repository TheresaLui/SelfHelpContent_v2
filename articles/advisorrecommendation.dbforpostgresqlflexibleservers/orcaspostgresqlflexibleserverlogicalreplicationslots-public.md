<properties
    pageTitle="Improve PostgreSQL performance by removing inactive logical replication slots"
    description="Improve PostgreSQL performance by removing inactive logical replication slots"
    authors="ramnov"
    ms.author="ramch"
    articleId="33f26810-57d0-4612-85ff-a83ee9be884a_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Remove inactive logical replication slots to improve PostgreSQL server performance
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "33f26810-57d0-4612-85ff-a83ee9be884a",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForPostgresql/flexibleServers",
  "recommendationFriendlyName": "OrcasPostgreSqlFlexibleServerLogicalReplicationSlots",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "orcasql-livesite@service.microsoft.com",
    "icm": {
      "routingId": "AIMS://AZURE OSS DATABASES/Open Source RDBMS",
      "service": "Azure OSS Databases",
      "team": "Open Source RDBMS - Breadth DRI"
    },
    "serviceTreeId": "c2c299e4-1a8f-4e90-9c0a-934e5ea8fc66"
  },
  "ingestionClientIdentities": [
    "49ebada5-bdc9-4c9b-826c-3cb789357c5d"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/azure_postgresql_flexible_server_logical_decoding",
  "description": "Improve PostgreSQL performance by removing inactive logical replication slots",
  "longDescription": "Our internal telemetry indicates that your PostgreSQL server may have inactive logical replication slots. This can result in reduced performance and server unavailability. To improve performance, we recommend that you either delete the inactive replication slots, or start using the slots so that the Log Sequence Number advances.",
  "potentialBenefits": "Improve PostgreSQL server performance by removing inactive logical replication slots",
  "actions": [
    {
      "actionId": "bb2f7bbc-dae3-46a1-b7c8-6416cd810240",
      "description": "How to drop a logical replication slot",
      "actionType": "Document",
      "documentLink": "https://aka.ms/azure_postgresql_flexible_server_logical_decoding"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "7df52e3b-7ca7-4e49-98f8-f503ba32f5af",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Remove inactive logical replication slots",
  "additionalColumns": [],
  "tip": "You can improve your PostgreSQL server performance by removing inactive logical replication slots."
}
---