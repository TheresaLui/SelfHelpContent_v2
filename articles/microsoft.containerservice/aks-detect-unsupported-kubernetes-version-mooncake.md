<properties
    pageTitle="Unsupported Kubernetes version is detected"
    description="Unsupported Kubernetes version is detected"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="962df50c-6b77-41bd-a432-f7f3611d1a29_mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="Compute_AzureKubernetesService"
/>

# Unsupported Kubernetes version is detected
---
{
  "recommendationOfferingId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "462b5f77-4a65-4287-885b-01a0f471743f",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('akscn.kusto.chinacloudapi.cn').database('AKSprod').UnsupportedKubernetesVersions",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.ContainerService/managedClusters",
  "recommendationFriendlyName": "UnsupportedKubernetesVersionIsDetected",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "potentialBenefits": "Ensure Kubernetes cluster runs with a supported version.",
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
  "version": 1.1,
  "description": "Unsupported Kubernetes version is detected",
  "longDescription": "Unsupported Kubernetes version is detected. Ensure Kubernetes cluster runs with a supported version.",
  "actions": [
    {
      "actionId": "9fcf30db-e1e0-4fe6-b933-cd65b2feab7c",
      "description": "Unsupported Kubernetes version is detected",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-supported-versions"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "0c9c9ab7-c0aa-4224-988d-b6bb05714d53",
    "actionType": "Blade",
    "bladeName": "ResourceMenuBlade",
    "extensionName": "HubsExtension",
    "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Unsupported Kubernetes version is detected",
  "additionalColumns": [],
  "learnMoreLink": "https://aka.ms/aks-supported-versions"
}
---
