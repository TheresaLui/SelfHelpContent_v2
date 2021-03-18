<properties
    pageTitle="Drop and recreate your HDInsight clusters to apply critical updates"
    description="Drop and recreate your HDInsight clusters to apply critical updates"
    authors="xunwei"
    ms.author="xunwei"
    articleId="d3a6303c-ac8f-4a9c-aad9-939b440d17ba_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_HDInsight"
/>
# Drop and recreate your HDInsight clusters to apply critical updates
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "d3a6303c-ac8f-4a9c-aad9-939b440d17ba",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsightff.kusto.usgovcloudapi.net').database('HDInsightFF').GCSCertRotationR3DropRecreate",
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "GCSCertRotationR3DropRecreate",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "hdicp@microsoft.com",
    "icm": {
      "routingId": "MDM://ControlPlane",
      "service": "HDInsight",
      "team": "Control Plane"
    },
    "serviceTreeId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters",
  "description": "Drop and recreate your HDInsight clusters to apply critical updates",
  "longDescription": "The HDInsight service has attempted to apply a critical certificate update on all your running clusters. However, due to some custom configuration changes, we are unable to apply the certificate updates on some of your clusters. Please drop and recreate your cluster before Jan 25th, 2021 to prevent the cluster from becoming unhealthy and unusable. ",
  "potentialBenefits": "Ensure cluster health and stability",
  "actions": [
    {
      "actionId": "d2461b4a-b127-4140-bb03-84ae165baae4",
      "description": "Please drop and recreate your cluster before Jan 25th, 2021 to prevent the cluster from becoming unhealthy and unusable.",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "0f8a0eab-4387-4ec6-9bd0-fba79f19d499",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Drop and recreate your HDInsight clusters to apply critical updates",
  "additionalColumns": [],
  "tip": "Drop and recreate your HDInsight clusters to apply critical updates",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/umahbase1rg/providers/Microsoft.HDInsight/clusters/umahbase1"
}
---
