<properties
    pageTitle="Update statistics on table columns"
    description="Update statistics on table columns"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="01dea77b-3ca4-4583-9b09-88f5a8fd5857_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Update statistics on table columns
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "SQL Data Warehouse",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "01dea77b-3ca4-4583-9b09-88f5a8fd5857",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/sqlDataWarehouses",
  "recommendationFriendlyName": "UpdateTableStatisticsSqlDW",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "aadevteam@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Azure Advisor",
      "team": "Azure Advisor"
    },
    "serviceTreeId": "f6d7f416-ee14-4943-894b-1abca9140b74"
  },
  "ingestionClientIdentities": [
    "b580d7a3-ef03-4330-913e-85a879b27bff",
    "d75d178b-baf7-43a2-8e98-49ba49ac7b2e"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/learnmorestatistics",
  "description": "Update statistics on table columns",
  "longDescription": "We have detected that you do not have up-to-date table statistics which may be impacting query performance. The query optimizer uses up-to-date statistics to estimate the cardinality or number of rows in the query result which enables the query optimizer to create a high quality query plan.",
  "potentialBenefits": "Increase query performance",
  "actions": [
    {
      "actionId": "ead27582-9549-42f3-881d-c21c2d3b2a12",
      "description": "Update table statistics",
      "actionType": "Document",
      "documentLink": "https://aka.ms/actionsupdatestatistics"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "06687182-7041-4cb3-a13c-30c5b6754dcf",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DataWarehouseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Update table statistics",
  "additionalColumns": [
    {
      "name": "impactedTableCount",
      "title": "Total Impacted Tables"
    }
  ]
}
---
