<properties
    pageTitle="Increase the PostgreSQL server vCores"
    description="Increase the PostgreSQL server vCores"
    authors="manishku"
    ms.author="kummanish"
    articleId="38500a53-575d-44b7-8f29-6cd534137438_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
/>
# Increase the PostgreSQL server vCores
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "38500a53-575d-44b7-8f29-6cd534137438",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlCpuOverload",
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
  "learnMoreLink": "https://aka.ms/postgresqlpricing",
  "description": "Increase the PostgreSQL server vCores",
  "longDescription": "Our internal telemetry shows that the CPU has been running under high utilization for an extended period of time over the last 7 days. High CPU utilization may lead to slow query performance. To improve performance, we recommend moving to a larger compute size.",
  "potentialBenefits": "Improve query performance by reducing CPU pressure",
  "actions": [
    {
      "actionId": "0d030a4e-cc56-4d33-b796-667eb722a284",
      "description": "Increase your server's CPU vCores",
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
      "actionId": "be37f88a-d22d-48be-94df-c435e7b481a1",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Increase the PostgreSQL server vCores",
  "additionalColumns": [],
  "tip": "You can improve the query performance of your PostgreSQL database by increasing the server vCores."
}
---
