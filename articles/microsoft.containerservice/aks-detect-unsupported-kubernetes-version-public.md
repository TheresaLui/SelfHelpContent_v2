<properties
    pageTitle="Unsupported Kubernetes version is detected"
    description="Unsupported Kubernetes version is detected"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="d6d466dd-1989-4c1b-b77e-f2d11c3e453c"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
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
    "streamNamespace": "cluster('aks.kusto.windows.net').database('AKSprod').UnsupportedKubernetesVersions",
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
  "version": 1.0,
  "description": "Unsupported Kubernetes version is detected",
  "longDescription": "Unsupported Kubernetes version is detected. Ensure Kubernetes cluster runs with a supported version.",
  "actions": [
    {
      "actionId": "c45debff-a78e-4b4f-9ee9-f310fc4fbc4d",
      "description": "Unsupported Kubernetes version is detected",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-supported-versions"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "aa264a9f-c171-49e4-addf-3006cd7d0bea",
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
