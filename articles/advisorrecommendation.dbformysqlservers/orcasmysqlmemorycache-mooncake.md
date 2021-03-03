<properties
    pageTitle="Move your MySQL server to Memory Optimized SKU"
    description="Move your MySQL server to Memory Optimized SKU"
    authors="ambhatna"
    ms.author="ambhatna"
    articleId="74aa92b7-9c42-4640-9b1b-8ab645c86a00_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Move your MySQL server to Memory Optimized SKU
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "74aa92b7-9c42-4640-9b1b-8ab645c86a00",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazurechi2.chinanorth2.kusto.chinacloudapi.cn').database('MoonCake').GetMySqlMemoryRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForMysql/servers",
  "recommendationFriendlyName": "OrcasMySQLMemoryCache",
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
  "learnMoreLink": "https://aka.ms/mysqlpricing",
  "description": "Move your MySQL server to Memory Optimized SKU",
  "longDescription": "Our internal telemetry shows that there is high churn in the buffer pool for this server which can result in slower query performance and increased IOPS. To improve performance, please review your workload queries to identify opportunities to minimize memory consumed.  If no such opportunity found, then we recommend moving to higher SKU with more memory or increase storage size to get more IOPS.",
  "potentialBenefits": "Improve query performance by caching more data in memory",
  "actions": [
    {
      "actionId": "6a628b58-6f98-408f-a20d-529451008bd4",
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
      "actionId": "ea185bb1-90e5-4b54-8ca6-1b284338b222",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Move your MySQL server to Memory Optimized SKU",
  "additionalColumns": [],
  "tip": "You can improve the query performance of your MySQL database by moving your server to a Memory Optimized SKU."
}
---
