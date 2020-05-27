<properties
    pageTitle="Convert tables to replicated tables with SQL Data Warehouse"
    description="Convert tables to replicated tables with SQL Data Warehouse"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="293984cf-b551-461f-b22d-9659ebd09a4f_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
	ownershipId="AzureData_AzureSQLDB_DataWarehouse"
/>
# Convert tables to replicated tables with SQL Data Warehouse
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "SQL Data Warehouse",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "293984cf-b551-461f-b22d-9659ebd09a4f",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').dw_advisor_ReplicatedTable",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/sqlDataWarehouses",
  "recommendationFriendlyName": "SqlDwReplicateTable",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "sqldwninjas@service.microsoft.com",
    "icm": {
      "routingId": "AIMS://AZURESQLDB/DATAWAREHOUSE/ADVISORS",
      "service": "Azure SQL DB",
      "team": "Datawarehouse"
    },
    "serviceTreeId": "6d302332-f404-4848-9509-b8a6b81510f7"
  },
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/learnmorereplicatedtables",
  "description": "Convert tables to replicated tables with SQL Data Warehouse",
  "longDescription": "We have detected that you may benefit from using replicated tables. When using replicated tables, this will avoid costly data movement operations and significantly increase the performance of your workload.",
  "potentialBenefits": "Increase query performance",
  "actions": [
    {
      "actionId": "0e5096ba-eb8e-443f-b137-79b0a2f1e017",
      "description": "Replicate Table",
      "actionType": "Document",
      "documentLink": "https://aka.ms/actionsreplicatetable"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "0e0a6dd0-28a4-44af-a0a0-178bf15f853c",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DataWarehouseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Replicate Table",
  "additionalColumns": [
    {
      "name": "TableName",
      "title": "Impacted Table"
    },
    {
      "name": "TableDetails",
      "title": "Details"
    }
  ],
  "tip": "You can improve your SQL Data Warehouse query performance by converting tables to replicated tables."
}
---
