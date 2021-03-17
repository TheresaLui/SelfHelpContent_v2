<properties
    pageTitle="Improve performance by optimizing MySQL temporary-table sizing"
    description="Improve performance by optimizing MySQL temporary-table sizing"
    authors="kummanish"
    ms.author="manishku"
    articleId="99811474-2a6c-4d40-ac91-ae76c76e3258_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
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
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').GetMySqlTmpTableRecommendations",
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
      "actionId": "dadf25c8-457f-45b0-8ef9-a328f020ce25",
      "description": "Increase value of Server Parameters: tmp_table_size, max_heap_table_size",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "MySqlServerParametersBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    },
    {
      "actionId": "1f918dc1-5a7e-4460-8d86-ea95c43a39aa",
      "description": "Optimally tuning your workload on Azure Database for MySQL",
      "actionType": "Document",
      "documentLink": "https://aka.ms/azure_mysql_tmp_table"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "72e6cc27-80d4-4e48-9881-2e3212e4367d",
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
