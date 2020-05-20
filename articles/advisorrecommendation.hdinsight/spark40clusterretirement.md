<properties
    pageTitle="Deprecation of Spark 2.3 in HDInsight 4.0 Spark cluster"
    description="Deprecation of Spark 2.3 in HDInsight 4.0 Spark cluster"
    authors="xunwei"
    ms.author="xunwei"
    articleId="663f0b55-0162-4451-a757-cc2c5a32af06_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="AzureData_HDInsight"
/>
# Deprecation of Spark 2.3 in HDInsight 4.0 Spark cluster 
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "663f0b55-0162-4451-a757-cc2c5a32af06",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').SparkVersionRetirementInHDI",
    "dataSource": "Kusto",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "SparkVersionRetirement",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "SparkDRI@microsoft.com",
    "icm": {
      "routingId": "MDM://HDISpark",
      "service": "HDInsight",
      "team": "Spark"
    },
    "serviceTreeId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/hdiretirespark",
  "description": "Deprecation of Spark 2.3 in HDInsight 4.0 Spark cluster ",
  "longDescription": "Starting from July 1 2020, customers will not be able to create new Spark clusters with Spark 2.3 on HDInsight 4.0. Existing clusters will run as is without the support from Microsoft. Consider moving to Spark 2.4 on HDInsight 4.0 by June 30 2020 to avoid potential system/support interruption.",
  "potentialBenefits": "Avoid potential system/support interruption.",
  "actions": [
    {
      "actionId": "9c12c552-0be9-4de3-b4b5-31469dedd276",
      "description": "Consider moving to Spark 2.4 on HDInsight 4.0 by June 30 2020 to avoid potential system/support interruption.",
      "actionType": "Document",
      "condition":"sparkComponentVersion==\"2.3\"",
      "documentLink": "https://aka.ms/hdiretirespark"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "4fc81805-6877-4d17-a987-dde5e7fe0e1f",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Deprecation of Spark 2.3 in HDInsight 4.0 Spark cluster ",
  "additionalColumns": [],
  "tip": "Deprecation of Spark 2.3 in HDInsight 4.0 Spark cluster ",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/sw-kafka/providers/Microsoft.HDInsight/clusters/sw-2340spark"
}
---
