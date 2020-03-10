<properties
    pageTitle="Use Accelerated Writes to Improve Write Performance"
    description="Use Accelerated Writes to Improve Write Performance"
    authors="xunwei"
    ms.author="xunwei"
    articleId="00774183-7be9-476d-93f6-98dedad70171"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Use Accelerated Writes to Improve Write Performance
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "00774183-7be9-476d-93f6-98dedad70171",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').HBaseClustersWithoutAcceleratedWrites",
    "dataSource": "Kusto",
    "refreshInterval": "08:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Low",
  "recommendationResourceType": "HDInsight",
  "recommendationFriendlyName": "AccWriteCandidate",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "hdistr@microsoft.com",
    "icm": {
      "routingId": "MDM://HDIStreaming",
      "service": "HDInsight",
      "team": "Streaming & Store (HBase, Phoenix, Kafka, Storm, OMS)"
    },
    "serviceTreeId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/en-us/azure/hdinsight/hbase/apache-hbase-accelerated-writes",
  "description": "Accelerated Writes uses Azure premium SSD managed disks to improve performance of your HBase cluster.",
  "longDescription": "The Accelerated Writes feature solves the problem of higher write-latencies caused by using Write Ahead Logs that are in cloud storage. The Accelerated Writes feature for HDInsight Apache HBase clusters, attaches premium SSD-managed disks to every RegionServer (worker node). Write Ahead Logs are then written to the Hadoop File System (HDFS) mounted on these premium managed-disks instead of cloud storage. Premium managed-disks use Solid-State Disks (SSDs) and offer excellent I/O performance with fault tolerance. Unlike unmanaged disks, if one storage unit goes down, it won't affect other storage units in the same availability set. As a result, managed-disks provide low write-latency and better resiliency for your applications.",
  "potentialBenefits": "Lower write-latency and better resiliency for your applications.",
  "actions": [
    {
      "actionId": "ee9d7ab4-ba29-47f6-bf78-eee5a2eb9cb7",
      "description": "Upgrade to Accelerated Writes to improve performance of your HBase cluster",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/en-us/azure/hdinsight/hbase/apache-hbase-accelerated-writes#how-to-enable-accelerated-writes-for-hbase-in-hdinsight"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "33498a9e-707a-4fc7-9ef1-64e76e0d6fe8",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Upgrade to Accelerated Writes to improve performance of your HBase cluster",
  "additionalColumns": [],
  "tip": "Upgrade to Accelerated Writes to improve performance of your HBase cluster",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/sw-shc/providers/Microsoft.HDInsight/clusters/sw-shchbase"
}
---
