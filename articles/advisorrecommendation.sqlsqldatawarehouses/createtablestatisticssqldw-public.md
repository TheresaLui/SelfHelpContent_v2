<properties
    pageTitle="Create statistics on table columns"
    description="Create statistics on table columns"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="ef14bcc2-41a5-41f6-bca8-10764cfbdee0_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Create statistics on table columns
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "SQL Data Warehouse",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "ef14bcc2-41a5-41f6-bca8-10764cfbdee0",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/sqlDataWarehouses",
  "recommendationFriendlyName": "CreateTableStatisticsSqlDW",
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
  "description": "Create statistics on table columns",
  "longDescription": "We have detected that you are missing table statistics which may be impacting query performance. The query optimizer uses statistics to estimate the cardinality or number of rows in the query result which enables the query optimizer to create a high quality query plan.",
  "potentialBenefits": "Increase query performance",
  "actions": [
    {
      "actionId": "469d0013-633e-4205-bc75-15c14ce40a9d",
      "description": "Create table statistics",
      "actionType": "Document",
      "documentLink": "https://aka.ms/actionscreatestatistics"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "16892249-c758-4ae3-8cba-fd5412fa1b7c",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DataWarehouseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Create table statistics",
  "additionalColumns": [
    {
      "name": "impactedTableCount",
      "title": "Total Impacted Tables"
    }
  ]
}
---
