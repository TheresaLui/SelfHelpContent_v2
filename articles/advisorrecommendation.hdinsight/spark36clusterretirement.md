<properties
    pageTitle="Deprecation of Spark 2.1 and 2.2 in HDInsight 3.6 Spark cluster"
    description="Deprecation of Spark 2.1 and 2.2 in HDInsight 3.6 Spark cluster"
    authors="xunwei"
    ms.author="xunwei"
    articleId="dd5fa7a3-8c14-4878-acbb-0f99df5e1c48_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="AzureData_HDInsight"
/>
# Deprecation of Spark 2.1 and 2.2 in HDInsight 3.6 Spark cluster 
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "dd5fa7a3-8c14-4878-acbb-0f99df5e1c48",
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
  "description": "Deprecation of Spark 2.1 and 2.2 in HDInsight 3.6 Spark cluster",
  "longDescription": "Starting from July 1 2020, customers will not be able to create new Spark clusters with Spark 2.1 and 2.2 on HDInsight 3.6. Existing clusters will run as is without the support from Microsoft. Consider to move to Spark 2.3 on HDInsight 3.6 by June 30 2020 to avoid potential system/support interruption.",
  "potentialBenefits": "Avoid potential system/support interruption.",
  "actions": [
    {
      "actionId": "715827a9-7710-4403-b291-659d137cc452",
      "description": "Consider to move to Spark 2.3 on HDInsight 3.6 by June 30 2020 to avoid potential system/support interruption. {extendedProperties}, {extendedProperties}.sparkComponentVersion",
      "actionType": "Document",
      "condition":"sparkComponentVersion!="2.3"",
      "documentLink": "https://aka.ms/hdiretirespark"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "8af9ef55-4ec5-409b-9812-eda55d78981f",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Deprecation of Spark 2.1 and 2.2 in HDInsight 3.6 Spark cluster",
  "additionalColumns": [],
  "tip": "Deprecation of Spark 2.1 and 2.2 in HDInsight 3.6 Spark cluster",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/sw-kafka/providers/Microsoft.HDInsight/clusters/sw-2236spark"
}
---
