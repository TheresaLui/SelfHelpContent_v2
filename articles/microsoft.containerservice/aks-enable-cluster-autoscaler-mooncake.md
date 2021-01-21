<properties
    pageTitle="Enable Cluster Autoscaler"
    description="Enable Cluster Autoscaler"
    authors="jomore"
    ms.author="jomore"
    articleId="71e42972-ea00-4529-be2b-17e087502e91_mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
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
    "streamNamespace": "cluster('akscn.kusto.chinacloudapi.cn').database('AKSprod').ClusterAutoscalerDisabled",
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
      "actionId": "44306708-bb90-4746-a740-0ec5f88e842f",
      "description": "Enable AKS Cluster Autoscaler",
      "actionType": "Document",
      "documentLink": "https://docs.azure.cn/aks/cluster-autoscaler"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "e002bc7d-6fc2-4dbb-a736-21cb492b17be",
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
  "learnMoreLink": "https://docs.azure.cn/aks/cluster-autoscaler"
}
---