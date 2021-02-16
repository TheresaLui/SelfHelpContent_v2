<properties
    pageTitle="Tuning the scan queries"
    description="Tuning the scan queries"
    authors="ramvasu"
    ms.author="ramvasu"
    articleId="09fa655c-8e0b-44fa-9236-e2021c0e7016_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_HDInsight"
/>
# Improving scan query performance
---
{
  "recommendationOfferingId": "f69bb3c8-af77-4bae-8894-7f866c5b693d",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "3b6f9784-2bf9-4348-a1e6-4554504f213d",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').AccWriteCandidateHBaseClusters",
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "ScanQueryTuningcandidate",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "hdistr@microsoft.com",
    "icm": {
      "routingId": "MDM://HDIStreaming",
      "service": "HDInsight",
      "team": "Streaming & Store (HBase, Phoenix, Kafka, Storm, OMS)"
    },
    "serviceTreeId": "feeb91fb-3ac7-43b9-8d2e-2290db2173f6"
  },
  "ingestionClientIdentities": [],
  "version": 2.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-advisor",
  "description": "More than 75% of your queries are full scan queries.",
  "longDescription": "More than 75% of the scan queries on your cluster are doing a full region/table scan. Modify your scan queries to avoid full region or table scans.",
  "potentialBenefits": "Faster scan performance",
  "actions": [
    {
      "actionId": "bf11f4ca-c126-4a60-9d9f-dc93b7ba161d",
      "description": "Revisit your scan queries to avoid full table/region scans",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-advisor#full-table-scan"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "e7ccec86-0195-4806-b1cf-e65532e0467c",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Revisit your scan queries",
  "additionalColumns": [],
  "tip": "Set start and stop rows to scans",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/blr_hbase/providers/Microsoft.HDInsight/clusters/hbase-216-writes-1-azuregraph"
}
---
