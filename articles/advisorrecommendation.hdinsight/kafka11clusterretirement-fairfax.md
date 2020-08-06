<properties
    pageTitle="Deprecation of Kafka 1.1 in HDInsight 4.0 Kafka Cluster"
    description="Deprecation of Kafka 1.1 in HDInsight 4.0 Kafka Cluster"
    authors="xunwei"
    ms.author="xunwei"
    articleId="36dff9ef-afde-40f5-b742-79a0bafcf6c2_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_HDInsight"
/>
# Deprecation of Kafka 1.1 in HDInsight 4.0 Kafka cluster
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "36dff9ef-afde-40f5-b742-79a0bafcf6c2",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').KafkaVersionRetirementInHDI",
    "dataSource": "Kusto",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "KafkaVersionRetirement",
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
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/hdiretirekafka",
  "description": "Deprecation of Kafka 1.1 in HDInsight 4.0 Kafka cluster",
  "longDescription": "Starting July 1, 2020, customers will not be able to create new Kafka clusters with Kafka 1.1 on HDInsight 4.0. Existing clusters will run as is without support from Microsoft. Consider moving to Kafka 2.1 on HDInsight 4.0 by June 30 2020 to avoid potential system/support interruption.",
  "potentialBenefits": "Avoid potential system/support interruption",
  "actions": [
    {
      "actionId": "14331419-3642-4a98-94a8-a9bff5530222",
      "description": "Consider moving to Kafka 2.1 on HDInsight 4.0 by June 30 2020 to avoid potential system/support interruption.",
      "actionType": "Document",
      "documentLink": "https://aka.ms/hdiretirekafka"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "bea4f667-0632-4b5f-b346-28540c415cac",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Deprecation of Kafka 1.1 in HDInsight 4.0 Kafka cluster",
  "additionalColumns": [],
  "tip": "Deprecation of Kafka 1.1 in HDInsight 4.0 Kafka cluster",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/sw-kafka/providers/Microsoft.HDInsight/clusters/sw-4011kafka"
}
---
