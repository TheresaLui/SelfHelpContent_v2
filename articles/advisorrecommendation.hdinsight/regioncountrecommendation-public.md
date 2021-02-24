<properties
    pageTitle="Region count tuning"
    description="Tune the region count/heap size"
    authors="ramvasu"
    ms.author="ramvasu"
    articleId="22a48d7e-085f-4cb8-8028-a4d41b23ed22_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_HDInsight"
/>
# Tune the RegionServer's region count for write performance
---
{
  "recommendationOfferingId": "8453f9b7-6eed-4504-a667-d1e93c3dfd73",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "076f2cce-a86e-4175-adba-4a7456839a47",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').HBase_updateBlockedTime",
    "dataSource": "Kusto",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "RegionCountCandidate",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "hdistr@microsoft.com",
    "icm": {
      "routingId": "MDM://HDIStreaming",
      "service": "HDInsight",
      "team": "Streaming & Store (HBase, Phoenix, Kafka, Storm, OMS)"
    },
    "serviceTreeId": "10491829-3504-456f-8f55-9238daefa8e1"
  },
  "ingestionClientIdentities": [],
  "version": 2.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-advisor",
  "description": "Check your region counts as you have blocking updates.",
  "longDescription": "Region counts needs to be adjusted to avoid updates getting blocked. It might require a scale up of the cluster by adding new nodes.",
  "potentialBenefits": "Brings more parallelism and ensures writes are more uniform.",
  "actions": [
    {
      "actionId": "bfff1cc7-5e25-46db-be41-496b8a08bed0",
      "description": "Tune the region count per region server",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-advisor#region-count-tuning"
    }
  ],
  "displayLabel": "Region count tuning.",
  "additionalColumns": [],
  "tip": "Tune the cluster based on the number of regions",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/blr_hbase/providers/Microsoft.HDInsight/clusters/hbase-216-writes"
}
---
