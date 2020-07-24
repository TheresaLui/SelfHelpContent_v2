<properties
    pageTitle="Move your MariaDB server to Memory Optimzed SKU"
    description="Move your MariaDB server to Memory Optimzed SKU"
    authors="manishku"
    ms.author="kummanish"
    articleId="a092afdb-6f20-4b42-8d8f-423ac8d71a3f_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
	  ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Move your MariaDB server to Memory Optimzed SKU
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a092afdb-6f20-4b42-8d8f-423ac8d71a3f",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').GetMariaDBMemoryRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForMariadb/servers",
  "recommendationFriendlyName": "OrcasMariaDbMemoryCache",
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
  "learnMoreLink": "https://aka.ms/mariadbpricing",
  "description": "Move your MariaDB server to Memory Optimzed SKU",
  "longDescription": "Our internal telemetry shows that there is high churn in the buffer pool for this server which can result in slower query performance and increased IOPS. To improve performance, please review your workload queries to identify opportunities to minimize memory consumed.  If no such opportunity found, then we recommend moving to higher SKU with more memory or increase storage size to get more IOPS.",
  "potentialBenefits": "Improve query performance by caching more data in memory",
  "actions": [
    {
      "actionId": "4e2378d5-62b7-48bf-87f6-91d697e32f56",
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
      "actionId": "894e0a1d-dec9-4339-b9a4-6f41b081d708",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Move your MariaDB server to Memory Optimzed SKU",
  "additionalColumns": [],
  "tip": "You can improve the query performance of your MariaDB database by moving your server to a Memory Optimized SKU."
}
---
