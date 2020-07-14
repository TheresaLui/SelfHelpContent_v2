<properties
    pageTitle="Improve performance by optimizing MySQL temporary-table sizing"
    description="Improve performance by optimizing MySQL temporary-table sizing"
    authors="alau"
    ms.author="alau-ms"
    articleId="99811474-2a6c-4d40-ac91-ae76c76e3258_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
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
    "streamNamespace": "cluster('https://sqlazureusg.kusto.usgovcloudapi.net').database('FairFax').GetMySqlTmpTableRecommendations",
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
  "ingestionClientIdentities": [
    "49ebada5-bdc9-4c9b-826c-3cb789357c5d"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/azure_mysql_tmp_table",
  "description": "Improve performance by optimizing MySQL temporary-table sizing",
  "longDescription": "Our internal telemetry indicates that your MySQL server may be incurring unncessary I/O overhead due to low temporary-table parameter settings. This may result in unnecessary disk-based transactions and reduced performance. We recommend that you increase the 'tmp_table_size' and 'max_heap_table_size' parameter values to reduce the number of disk-based transactions.",
  "potentialBenefits": "Improve MySQL workload performance by reducing I/O overhead associated with disk-based transactions",
  "actions": [
    {
      "actionId": "a6c2cd8a-bd92-4aa1-bb9c-fc7ac4db3a94",
      "description": "Increase value of Server Parameters: tmp_table_size, max_heap_table_size",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "MySqlServerParametersBlade",
      "metadata": {
      "resourceId": "{resourceId}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "78e7e4b9-bac2-47bc-92da-6979eba19b7d",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "MySqlServerParametersBlade",
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
