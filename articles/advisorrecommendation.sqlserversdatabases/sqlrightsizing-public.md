<properties
    pageTitle="Right-size underutilized SQL Databases"
    description="Right-size underutilized SQL Databases"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="b83241d3-47ba-4603-8d5a-a1b3331e74f4_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Right-size underutilized SQL Databases
---
{
  "recommendationOfferingId": "1c017867-b3d9-4798-979e-9693c49579f8",
  "recommendationOfferingName": "Azure SQL Database",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "b83241d3-47ba-4603-8d5a-a1b3331e74f4",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "AzureAdvisor.SQLRightSizingFilteredIn_Public",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Sql/servers/databases",
  "recommendationFriendlyName": "SQLRightSizing",
  "recommendationMetadataState": "Active",
  "recommendationScope": "Internal",
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
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/SQLDBrecommendation",
  "description": "Right-size underutilized SQL Databases",
  "longDescription": "We've analyzed the DTU consumption of your SQL Database over the past 14 days and identified SQL Databases with low usage. You can save money by right-sizing to the recommended SKU based on the 95th percentile of your every day workload.",
  "potentialBenefits": "Optimize Azure spend",
  "actions": [
    {
      "actionId": "2ba48c1d-e255-4b12-9f50-8458fdc2a677",
      "description": "Resize the SQL Database",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DatabaseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "302693dc-bee7-4d6c-9dfc-9f0d5f3b0976",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DatabaseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Right Size SQL DB",
  "additionalColumns": [
    {
      "name": "Recommended_SKU",
      "title": "Recommended SKU"
    },
    {
      "name": "ServerName",
      "title": "SQL Server Name"
    },
    {
      "name": "ObservationPeriodEndDate",
      "title": "Observation End Period"
    }
  ]
}
---
