<properties
    pageTitle="Scale the storage limit for PostgreSQL server"
    description="Scale the storage limit for PostgreSQL server"
    authors="manishku"
    ms.author="kummanish"
    articleId="ae2b8ab9-f6b9-4531-ba04-44f00880dc18_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="usnat"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Scale the storage limit for PostgreSQL server
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "ae2b8ab9-f6b9-4531-ba04-44f00880dc18",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').GetPostgreSqlStorageRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlStorageLimit",
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
  "learnMoreLink": "https://aka.ms/postgresqlstoragelimits",
  "description": "Scale the storage limit for PostgreSQL server",
  "longDescription": "Our internal telemetry shows that the server may be constrained because it is approaching limits for the currently provisioned storage values. This may result in degraded performance or in the server being moved to read-only mode. To ensure continued performance, we recommend increasing the provisioned storage amount or turning ON the \"Auto-Growth\" feature for automatic storage increases",
  "potentialBenefits": "Improve query performance by allocating larger storage for the server",
  "actions": [
    {
      "actionId": "f07caf69-0c55-46d2-b0ce-0ebc10c64e9d",
      "description": "Increase Storage for your PostgreSQL Server",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "pricingTier"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "6dad6189-ee9c-4841-8a4f-1f6532d02b59",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Increase the Server Storage limit",
  "additionalColumns": []
}
---