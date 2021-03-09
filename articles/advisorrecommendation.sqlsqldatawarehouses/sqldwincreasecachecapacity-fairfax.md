<properties
    pageTitle="Scale up to optimize cache utilization with SQL Data Warehouse"
    description="Scale up to optimize cache utilization with SQL Data Warehouse"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="14b28bdb-b83d-4f55-a516-44d4152f1f2b_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="AzureData_SynapseAnalytics"
/>
# Scale up to optimize cache utilization with SQL Data Warehouse
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "Azure Synapse Analytics",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "14b28bdb-b83d-4f55-a516-44d4152f1f2b",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusg.kusto.usgovcloudapi.net').database('FairFax').dw_advisor_IncreaseCacheCapacity",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/sqlDataWarehouses",
  "recommendationFriendlyName": "SqlDwIncreaseCacheCapacity",
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
  "learnMoreLink": "https://aka.ms/learnmoreadaptivecache",
  "description": "Scale up to optimize cache utilization with SQL Data Warehouse",
  "longDescription": "We have detected that you had high cache used percentage with a low hit percentage. This indicates high cache eviction which can impact the performance of your workload.",
  "potentialBenefits": "Increase query performance",
  "actions": [
    {
      "actionId": "23f523a2-3556-4a0d-9ffc-bdab83ec26f3",
      "description": "Scale your data warehouse",
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
      "actionId": "cec5dc51-4d6d-4f63-bd4d-510970a7b702",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DataWarehouseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Increase Cache Capacity",
  "additionalColumns": [],
  "tip": "You can improve your SQL Data Warehouse query performance by scaling up to optimize cache utilization."
}
---
