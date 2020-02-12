<properties
    pageTitle="Scale up or update resource class to reduce tempdb contention with SQL Data Warehouse"
    description="Scale up or update resource class to reduce tempdb contention with SQL Data Warehouse"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="33e515fe-354c-4016-a0f7-c4d6585aea61_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
/>
# Scale up or update resource class to reduce tempdb contention with SQL Data Warehouse
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "SQL Data Warehouse",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "33e515fe-354c-4016-a0f7-c4d6585aea61",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusg.kusto.usgovcloudapi.net').database('FairFax').dw_advisor_TempdbContention",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/sqlDataWarehouses",
  "recommendationFriendlyName": "SqlDwReduceTempdbContention",
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
  "learnMoreLink": "https://aka.ms/learnmoretempdb",
  "description": "Scale up or update resource class to reduce tempdb contention with SQL Data Warehouse",
  "longDescription": "We have detected that you had high tempdb utilization which can impact the performance of your workload.",
  "potentialBenefits": "Increase query performance",
  "actions": [
    {
      "actionId": "31fe9531-8528-484f-8c54-76f68d7d7f9f",
      "description": "Scale your data warehouse or increase resource classes for your workload",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "ScaleDataWarehouseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "893107b9-b2c3-42b7-9ba2-b14ac02ff185",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DataWarehouseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Reduce Tempdb Contention",
  "additionalColumns": [],
  "tip": "You can improve your SQL Data Warehouse query performance by scaling up or updating your resource class to reduce tempdb contention."
}
---
