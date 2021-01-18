<properties
    pageTitle="Drop and recreate your HDInsight clusters to apply critical updates"
    description="Drop and recreate your HDInsight clusters to apply critical updates"
    authors="xunwei"
    ms.author="xunwei"
    articleId="69740e3e-5b96-4b0e-b9b8-4d7573e3611c_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_HDInsight"
/>
# Drop and recreate your HDInsight clusters to apply critical updates
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "69740e3e-5b96-4b0e-b9b8-4d7573e3611c",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').GCSCertRotationRound2",
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "GCSCertRotationRound2",
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
  "longDescription": "The HDInsight service has attempted to apply a critical certificate update on all your running clusters. However, due to some custom configuration changes, we are unable to apply the certificate updates on some of your clusters.",
  "potentialBenefits": "Ensure cluster health and stability",
  "actions": [
    {
      "actionId": "23eb24c2-a0ca-4c50-8d85-78f95fddb8c2",
      "description": "Please drop and recreate your cluster before Jan 25th, 2021 to prevent the cluster from becoming unhealthy and unusable. ",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "79383bbf-97e1-4f65-ac2a-63dc57aae12c",
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
