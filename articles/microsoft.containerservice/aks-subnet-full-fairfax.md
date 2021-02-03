<properties
    pageTitle="Cluster subnet is full"
    description="Cluster subnet is full"
    authors="jomore"
    ms.author="jomore"
    articleId="ca321631-e95c-4fde-a587-13158fb5f0c6_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="Compute_AzureKubernetesService"
/>

# Cluster subnet is full 
---
{
  "recommendationOfferingId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0",
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
  "recommendationFriendlyName": "NodeSubnetIsFull",
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
    "serviceTreeId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0"
  },
  "ingestionClientIdentities": [],
  "version": 3.1,
  "description": "The AKS node pool subnet is full",
  "longDescription": "Some of the subnets for this cluster's node pools are full and cannot take any more worker nodes. Using the Azure CNI plugin requires to reserve IP addresses for each node and all the pods for the node at node provisioning time. If there is not enough IP address space in the subnet, no worker nodes can be deployed. Additionally, the AKS cluster cannot be upgraded if the node subnet is full.",
  "actions": [
    {
      "actionId": "e91c559b-75c6-4788-82d3-61ff2f7738da",
      "description": "Recreate the cluster in a larger subnet, or add new node pools to the clusters in additional subnets",
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
