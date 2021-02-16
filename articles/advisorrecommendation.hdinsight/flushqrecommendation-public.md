<properties
    pageTitle="Flush related tuning"
    description="Tune the flusher threads"
    authors="ramvasu"
    ms.author="ramvasu"
    articleId="53af2425-8287-4ca5-a5da-b84de9af4f42_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_HDInsight"
/>
# Tune the RegionServer's flush queue for write performance
---
{
  "recommendationOfferingId": "121511ec-ea64-4428-80b0-7d59f2c8fd49",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "469b5242-26ee-4a4c-ba65-97479166bcf1",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').HBase_flushQueueLength",
    "dataSource": "Kusto",
    "refreshInterval": "05:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "FlushQueueCandidate",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "hdistr@microsoft.com",
    "icm": {
      "routingId": "MDM://HDIStreaming",
      "service": "HDInsight",
      "team": "Streaming & Store (HBase, Phoenix, Kafka, Storm, OMS)"
    },
    "serviceTreeId": "36e3ae94-0955-49ef-801c-da42a638ff35"
  },
  "ingestionClientIdentities": [],
  "version": 2.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-advisor",
  "description": "Consider increasing the flusher threads",
  "longDescription": "The flush queue size in your region servers are more than 100 or there are updates getting blocked frequently. Tuning of the flush handler is recommended.",
  "potentialBenefits": "Faster flushes would clear the writes from being blocked.",
  "actions": [
    {
      "actionId": "0418c795-f936-494d-9cae-cd1bc98f4061",
      "description": "Consider increasing the flush handler count",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-advisor#optimize-the-flush-queue"
    }
  ],
  "displayLabel": "Tuning the flushes",
  "additionalColumns": [],
  "tip": "Increase flush handler count to improve write performance",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/blr_hbase/providers/Microsoft.HDInsight/clusters/hbase-216-writes"
}
---
