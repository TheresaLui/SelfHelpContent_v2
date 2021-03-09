<properties
    pageTitle="Improve performance by optimizing MySQL temporary-table sizing"
    description="Improve performance by optimizing MySQL temporary-table sizing"
    authors="alau"
    ms.author="alau-ms"
    articleId="99811474-2a6c-4d40-ac91-ae76c76e3258_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Improve performance by optimizing MySQL temporary-table sizing
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "99811474-2a6c-4d40-ac91-ae76c76e3258",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazurechi2.chinanorth2.kusto.chinacloudapi.cn').database('MoonCake').GetMySqlTmpTableRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForMySql/servers",
  "recommendationFriendlyName": "OrcasMySqlTmpTables",
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
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/azure_mysql_tmp_table",
  "description": "Improve performance by optimizing MySQL temporary-table sizing",
  "longDescription": "Our internal telemetry indicates that your MySQL server may be incurring unnecessary I/O overhead due to low temporary-table parameter settings. This may result in unnecessary disk-based transactions and reduced performance. We recommend that you increase the 'tmp_table_size' and 'max_heap_table_size' parameter values to reduce the number of disk-based transactions.",
  "potentialBenefits": "Improve MySQL workload performance by reducing I/O overhead associated with disk-based transactions",
  "actions": [
    {
      "actionId": "c7225d5a-5ca0-4dc9-9f49-af16cb1d7e96",
      "description": "Increase value of Server Parameters: tmp_table_size, max_heap_table_size",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "MySqlServerParametersBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    },
    {
      "actionId": "67156fc8-068c-4ba7-ad0e-cb73f5848c04",
      "description": "Optimally tuning your workload on Azure Database for MySQL",
      "actionType": "Document",
      "documentLink": "https://aka.ms/azure_mysql_tmp_table"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "2d426d97-87ed-4e43-a749-efae8fa67569",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Improve performance by optimizing MySQL temporary-table sizing",
  "additionalColumns": [],
  "tip": "You can adjust your MySQL temporary-table sizing to improve database performance."
}
---
