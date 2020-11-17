<properties
    pageTitle="Split staged files in the storage account to increase load performance"
    description="Split staged files in the storage account to increase load performance"
    authors="kevin"
    ms.author="kevin"
    articleId="dd93fbbf-e5ef-4c7c-886e-2bfef0958f45_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
    ownershipId="AzureData_SynapseAnalytics"
/>

# Split staged files in the storage account to increase load performance
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "Azure Synapse Analytics",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "dd93fbbf-e5ef-4c7c-886e-2bfef0958f45",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').dw_advisor_Load_FileSplits",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/sqlDataWarehouses",
  "recommendationFriendlyName": "FileSplittingGuidance",
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
  "learnMoreLink": "https://aka.ms/learnmorefilesplit",
  "description": "Split staged files in the storage account to increase load performance",
  "longDescription": "We have detected that you can increase load throughput by splitting your compressed files that are staged in your storage account. A good rule of thumb is to split compressed files into 60 or more to maximize the parallelism of your load. ",
  "potentialBenefits": "Increase load performance",
  "actions": [
    {
      "actionId": "a3d2fde3-52ff-44e8-8260-51db7a14621f",
      "description": "Split files that are staged for loading",
      "actionType": "Document",
      "documentLink": "https://aka.ms/learnmorefilesplit"
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
  "displayLabel": "Split files that are staged for loading",
  "additionalColumns": [],
  "tip": "You can improve load performance by splitting files that are staged for loading.",
  "testData":"5a352e58-10ee-4f0f-9ce7-c6de232fc8ac,/subscriptions/5a352e58-10ee-4f0f-9ce7-c6de232fc8ac/resourceGroups/DWRJobs/providers/Microsoft.Sql/servers/dwreliability/databases/DWReliability"

}
---
