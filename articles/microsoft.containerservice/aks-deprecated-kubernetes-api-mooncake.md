<properties
    pageTitle="Deprecated Kubernetes API in 1.16 is found"
    description="Deprecated Kubernetes API in 1.16 is found"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="3300f699-b6ec-40bc-aede-5d9125bff82c"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="Compute_AzureKubernetesService"
/>

# Deprecated Kubernetes API in 1.16 is found
---
{
  "recommendationOfferingId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "ac304dbf-3b56-47f0-8271-d7eac8991e16",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('akscn.kusto.chinacloudapi.cn').database('AKSprod').DeprecatedKubernetesAPI116",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.ContainerService/managedClusters",
  "recommendationFriendlyName": "DeprecatedKubernetesAPIIn116IsFound",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "potentialBenefits": "Avoid using deprecated API",
  "owner": {
    "email": "aksoverlay@microsoft.com",
    "icm": {
      "routingId": "MDM://ACSRP",
      "service": "Azure Kubernetes Service",
      "team": "RP"
    },
    "serviceTreeId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "description": "Deprecated Kubernetes API in 1.16 is found",
  "longDescription": "Deprecated Kubernetes API in 1.16 is found. Avoid using deprecated API.",
  "actions": [
    {
      "actionId": "42d1c454-c9aa-4fa9-9b11-ae4e8f0fd95a",
      "description": "Deprecated Kubernetes API in 1.16 is found",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-deprecated-k8s-api-1.16"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "53ac1fb3-9efd-459a-88d5-bd16eb742397",
    "actionType": "Blade",
    "bladeName": "ResourceMenuBlade",
    "extensionName": "HubsExtension",
    "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Deprecated Kubernetes API in 1.16 is found",
  "additionalColumns": [],
  "learnMoreLink": "https://aka.ms/aks-deprecated-k8s-api-1.16"
}
---
