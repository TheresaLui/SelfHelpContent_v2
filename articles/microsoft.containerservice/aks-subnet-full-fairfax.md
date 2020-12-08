<properties
    pageTitle="Cluster subnet is full"
    description="Cluster subnet is full"
    authors="jomore"
    ms.author="jomore"
    articleId="ca321631-e95c-4fde-a587-13158fb5f0c6_fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="Compute_AzureKubernetesService"
/>

# Cluster subnet is full 
---
{
  "recommendationOfferingId": "0b9258da-c7d5-4a04-8eb6-01283c4c72e5",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "15a9b3c0-138b-4141-8bcc-8d8f5a5b91a6",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('aksff.kusto.usgovcloudapi.net').database('AKSprod').PoolSubnetFull",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.ContainerService/managedClusters",
  "recommendationFriendlyName": "Node subnet is full",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "potentialBenefits": "You need to expand your cluster with additional node pools to be able to grow",
  "owner": {
    "email": "jomore@microsoft.com",
    "icm": {
      "routingId": "MDM://ACSRP",
      "service": "Azure Kubernetes Service",
      "team": "Azure Kubernetes Service"
    },
    "serviceTreeId": "e73183be-4979-48e7-8fd9-7bdcda5748c0"
  },
  "ingestionClientIdentities": [],
  "version": 1.1,
  "description": "Pool subnet is full",
  "longDescription": "Some of the subnets for this cluster's nodepools are full and cannot take more worker nodes",
  "actions": [
    {
      "actionId": "e91c559b-75c6-4788-82d3-61ff2f7738da",
      "description": "Recreate the cluster in a larger subnet, or add new nodepools to the clusters in additional subnets",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/aks/use-multiple-node-pools#add-a-node-pool-with-a-unique-subnet-preview"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "123add3f-8b1d-4d80-8210-3b0d5793c616",
      "actionType": "Blade",
      "bladeName": "ResourceMenuBlade",
      "extensionName": "HubsExtension",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Node subnet is full",
  "additionalColumns": [],
  "learnMoreLink": "https://docs.microsoft.com/azure/aks/use-multiple-node-pools#add-a-node-pool-with-a-unique-subnet-preview"
}
---
