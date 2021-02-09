<properties
    pageTitle="Compaction threads tuning"
    description="Tune the compaction threads for faster compactions"
    authors="ramvasu"
    ms.author="ramvasu"
    articleId="8c04c87d-f4b7-4991-a1c1-2f5fbe689d94_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_HDInsight"
/>
# Tune the RegionServer's compaction queue for read performance
---
{
  "recommendationOfferingId": "2c320048-aefd-4637-b82c-3b0fc8b84830",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "e459ed06-6204-4c85-9f75-9b046b68578a",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').HBase_compactionQueueLength",
    "dataSource": "Kusto",
    "refreshInterval": "05:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "CompactionQueueCandidate",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "hdistr@microsoft.com",
    "icm": {
      "routingId": "MDM://HDIStreaming",
      "service": "HDInsight",
      "team": "Streaming & Store (HBase, Phoenix, Kafka, Storm, OMS)"
    },
    "serviceTreeId": "d99d7c87-0d16-4269-a159-7534cc4795f1"
  },
  "ingestionClientIdentities": [],
  "version": 2.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-advisor",
  "description": "Consider increasing your compaction threads for compactions to complete faster",
  "longDescription": "The compaction queue in your region servers are more than 2000 suggesting that more data requires compaction. Slower compactions can impact read performance as the number of files to read are more. More files without compaction can also impact the heap usage related to how files interact with Azure file system.",
  "potentialBenefits": "Faster compactions would ensure faster reads and less heap usage.",
  "actions": [
    {
      "actionId": "d64e27e8-3b25-444e-9a81-feddf8937aad",
      "description": "Consider increasing the compaction threads count",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-advisor#compaction-queue-tuning"
    }
  ],
  "displayLabel": "Increasing compaction threads count",
  "additionalColumns": [],
  "tip": "Increase compaction thread count to improve read performance",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/blr_hbase/providers/Microsoft.HDInsight/clusters/hbase-216-writes"
}
---
