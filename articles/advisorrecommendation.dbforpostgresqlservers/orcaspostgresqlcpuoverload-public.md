<properties
    pageTitle="Increase the PostgreSQL server vCores"
    description="Increase the PostgreSQL server vCores"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="38500a53-575d-44b7-8f29-6cd534137438_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
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
      "actionId": "a8a4f36f-da0d-4bdc-8d32-a1f94c9c9db4",
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
      "actionId": "42d0dbf8-95ca-4668-acef-5c2177761338",
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
