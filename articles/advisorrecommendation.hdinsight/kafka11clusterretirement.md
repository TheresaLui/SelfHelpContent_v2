<properties
    pageTitle="Deprecation of Kafka 1.1 in HDInsight 4.0 Kafka cluster"
    description="Deprecation of Kafka 1.1 in HDInsight 4.0 Kafka cluster"
    authors="xunwei"
    ms.author="xunwei"
    articleId="5834ba65-bfd2-4ae1-8c8a-879c9e3e702e_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="AzureData_HDInsight"
/>
# Deprecation of Kafka 1.1 in HDInsight 4.0 Kafka cluster
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "5834ba65-bfd2-4ae1-8c8a-879c9e3e702e",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').Kafka11RetirementIn40HDI",
    "dataSource": "Kusto",
    "refreshInterval": "08:00:00"
  },
  "recommendationCategory": "Performance",
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
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/hdiretirekafka",
  "description": "Deprecation of Kafka 1.1 in HDInsight 4.0 Kafka cluster",
  "longDescription": "Starting from July 1 2020, customers will not be able to create new Kafka clusters with Kafka 1.1 on HDInsight 4.0. Existing clusters will run as is without the support from Microsoft. Consider moving to Kafka 2.1 on HDInsight 4.0 by June 30 2020 to avoid potential system/support interruption.",
  "potentialBenefits": "Avoid potential system/support interruption.",
  "actions": [
    {
      "actionId": "a9ddc83c-d228-4d8c-9a5f-efc2be9bc6ce",
      "condition":"ComponentVersion==""1.1""",
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