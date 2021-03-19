<properties
    pageTitle="Enable critical updates to be applied to your HDInsight clusters"
    description="Enable critical updates to be applied to your HDInsight clusters"
    authors="xunwei"
    ms.author="xunwei"
    articleId="cd31b398-afa9-40fb-875b-18737857198c_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_HDInsight"
/>
# Enable critical updates to be applied to your HDInsight clusters
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "cd31b398-afa9-40fb-875b-18737857198c",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsightff.kusto.usgovcloudapi.net').database('HDInsightFF').GCSCertRotation",
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "GCSCertRotation",
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
  "version": 2.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters",
  "description": "Enable critical updates to be applied to your HDInsight clusters",
  "longDescription": "HDInsight service is applying an important certificate related update to your cluster. However, one or more policies in your subscription are preventing HDInsight service from creating or modifying network resources (Load balancer, Network Interface and Public IP address) associated with your clusters and applying this update. Please take actions to allow HDInsight service to create or modify network resources (Load balancer, Network interface and Public IP address) associated with your clusters before Jan 13, 2021 05:00 PM UTC. The HDInsight team will be performing updates between Jan 13, 2021 05:00 PM UTC and Jan 16, 2021 05:00 PM UTC. Failure to apply this update may result in your clusters becoming unhealthy and unusable. ",
  "potentialBenefits": "Ensure cluster health and stability",
  "actions": [
    {
      "actionId": "050a15fa-ffb5-49ae-9994-d9f060d942f2",
      "description": "Please refresh your policy to allow HDInsight service to create or modify network resources (Load balancer, Network interface and Public IP address) associated with your clusters before Jan 13, 2021 05:00 PM UTC. You can also drop and recreate the cluster to apply the updates.",
      "actionType": "Document",
      "condition":"group==\"policy\"",
      "documentLink": "https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters"
    },
    {
      "actionId": "9d9127db-e388-4bef-a3f8-415d1067f811",
      "description": "Please unlock your cluster resource group to allow HDInsight service to create or modify network resources (Load balancer, Network interface and Public IP address) associated with your clusters before Jan 13, 2021 05:00 PM UTC. You can also drop and recreate the cluster to apply the updates.",
      "actionType": "Document",
      "condition":"group==\"template\"",
      "documentLink": "https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "af1bc219-3a05-4a5e-ab3a-ac1d81eeba16",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Enable critical updates to be applied to your HDInsight clusters",
  "additionalColumns": [],
  "tip": "Enable critical updates to be applied to your HDInsight clusters",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/sw-shc/providers/Microsoft.HDInsight/clusters/swtesthb,\"{\"\"group\"\" :\"\"policy\"\"}\""
}
---
