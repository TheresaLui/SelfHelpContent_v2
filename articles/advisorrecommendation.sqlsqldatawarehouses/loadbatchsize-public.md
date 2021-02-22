<properties
    pageTitle="Increase batch size when loading"
    description="Increase batch size when loading"
    authors="kevin"
    ms.author="kevin"
    articleId="e0ba1234-61da-46e3-a66d-fa0752b9df7d_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_SynapseAnalytics"
/>

# Increase batch size when loading to maximize load throughput, data compression, and query performance
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "Azure Synapse Analytics",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "e0ba1234-61da-46e3-a66d-fa0752b9df7d",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqladhoc.kusto.windows.net').database('sqlazure1').dw_advisor_Load_BatchSize",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/sqlDataWarehouses",
  "recommendationFriendlyName": "LoadBatchSizeGuidance",
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
  "learnMoreLink": "https://aka.ms/learnmoreincreasebatchsize",
  "description": "Increase batch size when loading to maximize load throughput, data compression, and query performance",
  "longDescription": "We have detected that you can increase load performance and throughput by increasing the batch size when loading into your database. You should consider using the COPY statement. If you are unable to use the COPY statement, consider increasing the batch size when using loading utilities such as the SQLBulkCopy API or BCP - a good rule of thumb is a batch size between 100K to 1M rows.",
  "potentialBenefits": "Increase load throughput, data compression, and query performance",
  "actions": [
    {
      "actionId": "a3d2fde3-52ff-44e8-8260-51db7a14621f",
      "description": "Increase batch size when loading to maximize load throughput, data compression, and query performance",
      "actionType": "Document",
      "documentLink": "https://aka.ms/learnmoreincreasebatchsize"
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
  "displayLabel": "Increase batch size when loading ",
  "additionalColumns": [],
  "tip": "You can improve load throughput, data compression, and query performance by increasing your batch size.",
  "testData":"5a352e58-10ee-4f0f-9ce7-c6de232fc8ac,/subscriptions/5a352e58-10ee-4f0f-9ce7-c6de232fc8ac/resourceGroups/DWRJobs/providers/Microsoft.Sql/servers/dwreliability/databases/DWReliability"

}
---
