<properties
    pageTitle="Move your MySQL server to Memory Optimized SKU"
    description="Move your MySQL server to Memory Optimized SKU"
    authors="manishku"
    ms.author="kummanish"
    articleId="4c16ae92-f40a-48ef-aeae-40aac7210a3e_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USSec"
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
    "streamNamespace": "cluster('https://sqlazureussece.usseceast.kusto.core.microsoft.scloud:443').database('sqlazure1').GetMySqlMemoryRecommendations",
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
      "actionId": "8ca57a5f-3aac-4975-b4ea-ef5dc22e239c",
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
      "actionId": "49f91887-82da-4d04-ad55-d33e09ec712c",
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
