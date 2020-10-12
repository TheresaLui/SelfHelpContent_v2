<properties
    pageTitle="Add a MySQL Read Replica server"
    description="Add a MySQL Read Replica server"
    authors="manishku"
    ms.author="kummanish"
    articleId="72cc5fbd-01c0-4a5b-8da4-f60d91c62962_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USSec"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Add a MySQL Read Replica server
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "1efe9592-f5ae-4167-97d7-63e973821fca",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureussece.usseceast.kusto.core.microsoft.scloud:443').database('sqlazure1').GetMySqlReadReplicaRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForMysql/servers",
  "recommendationFriendlyName": "OrcasMySQLReadReplica",
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
  "learnMoreLink": "https://aka.ms/mysqlreadreplica",
  "description": "Add a MySQL Read Replica server",
  "longDescription": "Our internal telemetry shows that you may have a read intensive workload running, which results in resource contention for this server. This may lead to slow query performance for the server. To improve performance, we recommend you add a read replica, and offload some of your read workloads to the replica.",
  "potentialBenefits": "Improve query performance by scaling out reads",
  "actions": [
    {
      "actionId": "5bc35b8e-1190-45f2-8d5a-f87ff7a42072",
      "description": "Scale out your read workload by adding a replica",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "MySqlServerReplicationBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "798ec205-b96a-4783-a7d6-843a64e3d2e6",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Add a MySQL Read Replica",
  "additionalColumns": [],
  "tip": "You can improve the query performance of your MySQL database my adding a Read Replica server."
}
---
