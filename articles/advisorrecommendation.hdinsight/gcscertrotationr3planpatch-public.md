<properties
    pageTitle="Apply critical updates to your HDInsight clusters"
    description="Apply critical updates to your HDInsight clusters"
    authors="xunwei"
    ms.author="xunwei"
    articleId="dddd213b-87b9-439e-a607-a9ecd94e0ae1_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_HDInsight"
/>
# Apply critical updates to your HDInsight clusters
---
{
  "recommendationOfferingId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "dddd213b-87b9-439e-a607-a9ecd94e0ae1",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').GCSCertRotationR3PlanPatch",
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "GCSCertRotationR3PlanPatch",
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
  "description": "Apply critical updates to your HDInsight clusters",
  "longDescription": "The HDInsight service has attempted to apply a critical certificate update on all your running clusters. However, one or more policies in your subscription are preventing HDInsight service from creating or modifying network resources (Load balancer, Network Interface and Public IP address) associated with your clusters and applying this update. Please remove or update your policy assignment to allow HDInsight service to create or modify network resources (Load balancer, Network interface and Public IP address) associated with your clusters before Jan 21, 2021 05:00 PM UTC. The HDInsight team will be performing updates between Jan 21, 2021 05:00 PM UTC and Jan 23, 2021 05:00 PM UTC. To verify the policy update, you can try to create network resources (Load balancer, Network interface and Public IP address) in the same resource group and Subnet where your cluster is in. Failure to apply this update may result in your clusters becoming unhealthy and unusable. You can also drop and recreate your cluster before Jan 25th, 2021 to prevent the cluster from becoming unhealthy and unusable. The HDInsight service will send another notification if we failed to apply the update to your clusters.",
  "potentialBenefits": "Ensure cluster health and stability",
  "actions": [
    {
      "actionId": "ce5a7772-fe3c-49d3-8d8f-076a69b9eef5",
      "description": "Please remove or update your policy assignment to allow HDInsight service to create or modify network resources (Load balancer, Network interface and Public IP address) associated with your clusters before Jan 21, 2021 05:00 PM UTC.",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "1a170a27-c18e-4707-9ccc-2327cebde32d",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Apply critical updates to your HDInsight clusters",
  "additionalColumns": [],
  "tip": "Apply critical updates to your HDInsight clusters",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/umahbase1rg/providers/Microsoft.HDInsight/clusters/umahbase1"
}
---
