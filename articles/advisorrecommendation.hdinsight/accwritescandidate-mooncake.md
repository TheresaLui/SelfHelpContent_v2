<properties
    pageTitle="Use Accelerated Writes to Improve Write Performance"
    description="Use Accelerated Writes to Improve Write Performance"
    authors="xunwei"
    ms.author="xunwei"
    articleId="8109a740-abe9-453e-91fc-c25598de73d0_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_HDInsight"
/>
# Use Accelerated Writes to Improve Write Performance
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "8109a740-abe9-453e-91fc-c25598de73d0",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsightmooncake2.chinanorth2.kusto.chinacloudapi.cn').database('HDInsightMC').AccWriteCandidateHBaseClusters",
    "dataSource": "Kusto",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
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
  "learnMoreLink": "https://docs.azure.cn/zh-cn/hdinsight/hbase/apache-hbase-accelerated-writes",
  "description": "Consider using Accelerated Writes feature in your HBase cluster to improve cluster performance.",
  "longDescription": "You are seeing this advisor recommendation because HDInsight team's system log shows that in the past 7 days, your cluster has encountered the following scenarios:\n\t1. High WAL sync time latency\n\t2. High write request count (at least 3 one hour windows of over 1000 avg_write_requests/second/node)\n\nThese conditions are indicators that your cluster is suffering from high write latencies. This could be due to heavy workload performed on your cluster.\nTo improve the performance of your cluster, you may want to consider utilizing the Accelerated Writes feature provided by Azure HDInsight HBase.  The Accelerated Writes feature for HDInsight Apache HBase clusters attaches premium SSD-managed disks to every RegionServer (worker node) instead of using cloud storage. As a result, provides low write-latency and better resiliency for your applications.\nTo read more on this feature, please visit link: ",
  "potentialBenefits": "Lower write-latency and better resiliency for your applications.",
  "actions": [
    {
      "actionId": "bf11f4ca-c126-4a60-9d9f-dc93b7ba161d",
      "description": "Consider upgrade to Accelerated Writes to improve performance of your HBase cluster",
      "actionType": "Document",
      "documentLink": "https://docs.azure.cn/zh-cn/hdinsight/hbase/apache-hbase-accelerated-writes#how-to-enable-accelerated-writes-for-hbase-in-hdinsight"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "5bde3f2b-2fc5-4bb4-af91-2edc7df7a6e8",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Consider upgrading to Accelerated Writes to improve performance of your HBase cluster",
  "additionalColumns": [],
  "tip": "Consider upgrading to Accelerated Writes to improve performance of your HBase cluster",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/sw-hbase/providers/Microsoft.HDInsight/clusters/sw-36hbase"
}
---
