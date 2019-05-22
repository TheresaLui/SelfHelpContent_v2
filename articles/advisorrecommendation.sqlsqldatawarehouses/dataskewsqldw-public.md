<properties
    pageTitle="Remove data skew to increase query performance"
    description="Remove data skew to increase query performance"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="9d7196d1-2d7c-4316-820f-7374a4ddf250_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Remove data skew to increase query performance
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "SQL Data Warehouse",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "9d7196d1-2d7c-4316-820f-7374a4ddf250",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/sqlDataWarehouses",
  "recommendationFriendlyName": "DataSkewSqlDW",
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
  "learnMoreLink": "https://aka.ms/learnmoredataskew",
  "description": "Remove data skew to increase query performance",
  "longDescription": "We have detected distribution data skew greater than 15%. This can cause costly performance bottlenecks.",
  "potentialBenefits": "Increase query performance",
  "actions": [
    {
      "actionId": "6b60034d-49e3-457b-891d-0967e1f5e2d7",
      "description": "Redistribute your data and revisit your table distribution key selections",
      "actionType": "Document",
      "documentLink": "https://aka.ms/actionsdataskew"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "2e9c45a5-3161-47b9-a0f8-13693b9b8a30",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DataWarehouseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Remove data skew",
  "additionalColumns": [
    {
      "name": "impactedTableCount",
      "title": "Total Impacted Tables"
    }
  ]
}
---
