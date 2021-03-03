<properties
    pageTitle="Move your PostgreSQL server to Memory Optimized SKU"
    description="Move your PostgreSQL server to Memory Optimized SKU"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="47b11ec4-7950-43a1-b6b5-f051f812bd34_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="usnat"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Move your PostgreSQL server to Memory Optimized SKU
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "47b11ec4-7950-43a1-b6b5-f051f812bd34",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').GetPostgreSqlMemoryRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlMemoryCache",
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
  "learnMoreLink": "https://aka.ms/postgresqlpricing",
  "description": "Move your PostgreSQL server to Memory Optimized SKU",
  "longDescription": "Our internal telemetry shows that there is high churn in the buffer pool for this server which can result in slower query performance and increased IOPS. To improve performance, please review your workload queries to identify opportunities to minimize memory consumed.  If no such opportunity found, then we recommend moving to higher SKU with more memory or increase storage size to get more IOPS.",
  "potentialBenefits": "Improve query performance by caching more data in memory",
  "actions": [
    {
      "actionId": "346872ee-b1db-484f-a645-362198b451c5",
      "description": "Increase your server's memory by scaling to a higher memory SKU",
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
      "actionId": "3d11a263-8b5d-4e03-a4b5-28bff1cc50d7",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Move your PostgreSQL server to Memory Optimized SKU",
  "additionalColumns": [],
  "tip": "You can improve the query performance of your PostgreSQL database by moving your server to a Memory Optimized SKU."
}
---
