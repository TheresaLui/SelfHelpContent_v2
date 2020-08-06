<properties
    pageTitle="Deprecation of Older Spark Versions in HDInsight Spark cluster"
    description="Deprecation of Older Spark Versions in HDInsight Spark cluster"
    authors="xunwei"
    ms.author="xunwei"
    articleId="20dfc768-7850-4176-9707-b9bb52afb95a_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_HDInsight"
/>
# Deprecation of Older Spark Versions in HDInsight Spark cluster 
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "20dfc768-7850-4176-9707-b9bb52afb95a",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').SparkVersionRetirementInHDI",
    "dataSource": "Kusto",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
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
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/hdiretirespark",
  "description": "Deprecation of Older Spark Versions in HDInsight Spark cluster",
  "longDescription": "Starting July 1, 2020, customers will not be able to create new Spark clusters with Spark 2.1 and 2.2 on HDInsight 3.6, and Spark 2.3 on HDInsight 4.0. Existing clusters will run as is without support from Microsoft. ",
  "potentialBenefits": "Avoid potential system/support interruption.",
  "actions": [
    {
      "actionId": "9c6eb9d0-a58d-4296-9b06-2028e81551e0",
      "description": "Consider moving to Spark 2.3 on HDInsight 3.6 by June 30 2020 to avoid potential system/support interruption.",
      "actionType": "Document",
      "condition":"sparkComponentVersion!=\"2.3\"",
      "documentLink": "https://aka.ms/hdiretirespark"
    },
    {
      "actionId": "086a57db-045c-4e33-9ef6-a539373ba565",
      "description": "Consider moving to Spark 2.4 on HDInsight 4.0 by June 30 2020 to avoid potential system/support interruption.",
      "actionType": "Document",
      "condition":"sparkComponentVersion==\"2.3\"",
      "documentLink": "https://aka.ms/hdiretirespark"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "8dc17d41-d715-4886-bd2a-26a13764b3c0",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Deprecation of Older Spark Versions in HDInsight Spark cluster",
  "additionalColumns": [],
  "tip": "Deprecation of Older Spark Versions in HDInsight Spark cluster",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/sw-kafka/providers/Microsoft.HDInsight/clusters/sw-2236spark"
}
---
