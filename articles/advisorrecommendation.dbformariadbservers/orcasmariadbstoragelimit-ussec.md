<properties
    pageTitle="Scale the storage limit for MariaDB server"
    description="Scale the storage limit for MariaDB server"
    authors="ambhatna"
    ms.author="ambhatna"
    articleId="dc791c8d-a74e-4b3e-b7f1-40793399ecd6_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="ussec"
    ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Scale the storage limit for MariaDB server
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "dc791c8d-a74e-4b3e-b7f1-40793399ecd6",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureussece.usseceast.kusto.core.microsoft.scloud').database('sqlazure1').GetMariaDBStorageRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForMariadb/servers",
  "recommendationFriendlyName": "OrcasMariaDbStorageLimit",
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
  "learnMoreLink": "https://aka.ms/mariadbstoragelimits",
  "description": "Scale the storage limit for MariaDB server",
  "longDescription": "Our internal telemetry shows that the server may be constrained because it is approaching limits for the currently provisioned storage values. This may result in degraded performance or in the server being moved to read-only mode. To ensure continued performance, we recommend increasing the provisioned storage amount or turning ON the \"Auto-Growth\" feature for automatic storage increases",
  "potentialBenefits": "Improve query performance by allocating larger storage for the server",
  "actions": [
    {
      "actionId": "15d0c46b-284f-4b59-9679-f28a9b8ebc29",
      "description": "Increase Storage for your MariaDB Server",
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
      "actionId": "affa4fc6-d9bc-4301-b37d-86f79405b54b",
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
