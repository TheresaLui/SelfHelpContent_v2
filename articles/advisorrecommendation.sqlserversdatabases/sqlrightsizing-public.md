<properties
    pageTitle="Right-size underutilized SQL Databases"
    description="Right-size underutilized SQL Databases"
    authors="raldaba"
    ms.author="aoaft"
    articleId="b83241d3-47ba-4603-8d5a-a1b3331e74f4_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
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
    "streamNamespace": "cluster('https://cerebro.centralus.kusto.windows.net').database('Publish').AzureAdvisor_Sql_SqlResizeReco",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Sql/servers/databases",
  "recommendationFriendlyName": "SQLRightSizing",
  "recommendationMetadataState": "Active",
  "recommendationScope": "Internal",
  "portalFeatures": [],
  "owner": {
    "email": "aoaft@microsoft.com",
    "icm": {
      "routingId": "AROTOOLBOX\\AROToolboxDevTeam",
      "service": "Azure Optimization Automation",
      "team": "Azure Optimization Automation"
    },
    "serviceTreeId": "a3db6cf3-640c-4340-8381-108d31853b7f"
  },
  "ingestionClientIdentities": [
    "6c75c76c-7792-4dd0-8e85-ad598f14bc93",
    "db97364d-48bf-4567-af34-e0843d0ee0af",
    "bd26e40e-c0cc-4d1d-8801-569dac0cd7fe",
    "9c14bff5-1bda-4de6-a74f-4c3caa370570"
  ],
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
  ],
  "costSavingInfo": "*You can save up to the stated amount if you choose to right-size your database. Your actual savings may vary."
}
---
