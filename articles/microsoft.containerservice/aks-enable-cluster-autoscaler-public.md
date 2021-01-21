<properties
    pageTitle="Enable Cluster Autoscaler"
    description="Enable Cluster Autoscaler"
    authors="jomore"
    ms.author="jomore"
    articleId="b44be6da-1b40-4c23-8630-fc1505156e18_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
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
    "streamNamespace": "cluster('aks.kusto.windows.net').database('AKSprod').ClusterAutoscalerDisabled",
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
      "actionId": "e002bc7d-6fc2-4dbb-a736-21cb492b17be",
      "description": "Enable AKS Cluster Autoscaler",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/aks/cluster-autoscaler"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "6646a29d-5714-4c9a-a226-9ea94fc1de8a",
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