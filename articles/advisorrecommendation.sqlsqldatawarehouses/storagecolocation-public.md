<properties
    pageTitle="Col-locate the storage account within the same region"
    description="Col-locate the storage account within the same region"
    authors="kevin"
    ms.author="kevin"
    articleId="314a2614-24d3-496c-b9d6-e6cd3df4b6c2"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_AzureSQLDB_DataWarehouse"
/>

# Co-locate the storage account within the same region to minimize latency when loading
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "SQL Data Warehouse",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "314a2614-24d3-496c-b9d6-e6cd3df4b6c2",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('sqladhoc.kustomfa.windows.net').database('sqlazure1').dw_advisor_Load_StorageAccount",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/sqlDataWarehouses",
  "recommendationFriendlyName": "ColocateStorageAccount",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "sqldwninjas@service.microsoft.com",
    "icm": {
      "routingId": "AIMS://AZURESQLDB/DATAWAREHOUSE/ADVISORS",
      "service": "Azure SQL DB",
      "team": "Datawarehouse"
    },
    "serviceTreeId": "6d302332-f404-4848-9509-b8a6b81510f7"
  },
  "ingestionClientIdentities": [ ],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/learnmorestoragecolocation",
  "description": "Co-locate the storage account within the same region to minimize latency when loading",
  "longDescription": "We have detected that you are loading from a region that is different from your SQL pool. You should consider loading from a storage account that is within the same region as your SQL pool to minimize latency when loading data.",
  "potentialBenefits": "Minimize latency and increase load performance",
  "actions": [
    {
      "actionId": "a3d2fde3-52ff-44e8-8260-51db7a14621f",
      "description": "Co-locate the storage account within the same region to minimize latency when loading",
      "actionType": "Document",
      "documentLink": "https://aka.ms/learnmorestoragecolocation"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "b98ae983-ef02-4d4e-9d73-ca67041bc3c3",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DataWarehouseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Colocate the storage account and the SQL pool within the same region",
  "additionalColumns": [],
  "tip": "You can minimize latency and increase load performance by colocating your storage account with your SQL pool",
  "testData":"5a352e58-10ee-4f0f-9ce7-c6de232fc8ac,/subscriptions/5a352e58-10ee-4f0f-9ce7-c6de232fc8ac/resourceGroups/DWRJobs/providers/Microsoft.Sql/servers/dwreliability/databases/DWReliability"

}
---
