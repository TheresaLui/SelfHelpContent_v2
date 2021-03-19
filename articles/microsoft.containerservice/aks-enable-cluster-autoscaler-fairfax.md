<properties
    pageTitle="Enable Cluster Autoscaler"
    description="Enable Cluster Autoscaler"
    authors="jomore"
    ms.author="jomore"
    articleId="f2126878-81d2-49d3-a159-2e8f19cc490b_fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="Compute_AzureKubernetesService"
/>

# Enable Cluster Autoscaler
---
{
  "recommendationOfferingId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c2f34a5d-2742-4c3d-9247-e0a8b85c3e51",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('aksff.kusto.usgovcloudapi.net').database('AKSprod').ClusterAutoscalerDisabled",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Low",
  "recommendationResourceType": "Microsoft.ContainerService/managedClusters",
  "recommendationFriendlyName": "EnableClusterAutoscaler",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "potentialBenefits": "Your cluster will scale up and down as required by workload resource demand",
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
  "version": 3.0,
  "description": "Enable the Cluster Autoscaler",
  "longDescription": "This cluster has not enabled AKS Cluster Autoscaler, and it will not adapt to changing load conditions unless you have other ways to autoscale your cluster",
  "actions": [
    {
      "actionId": "0bb5a35d-f0be-4115-95f0-144aee0d0cef",
      "description": "Enable AKS Cluster Autoscaler",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/aks/cluster-autoscaler"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "81926ac7-f097-46fd-b9a8-9a74f2e968b1",
      "actionType": "Blade",
      "bladeName": "ResourceMenuBlade",
      "extensionName": "HubsExtension",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Enable Cluster Autoscaler",
  "additionalColumns": [],
  "learnMoreLink": "https://docs.microsoft.com/azure/aks/cluster-autoscaler"
}
---