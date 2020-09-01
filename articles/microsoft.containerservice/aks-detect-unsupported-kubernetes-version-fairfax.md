<properties
    pageTitle="Unsupported Kubernetes version is detected"
    description="Unsupported Kubernetes version is detected"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="a12cf5e4-c3b3-44df-b365-8784f643453c"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
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
    "streamNamespace": "cluster('aksff.kusto.usgovcloudapi.net').database('AKSprod').UnsupportedKubernetesVersions",
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
      "actionId": "78370489-9a92-4d08-98eb-7800e8ff20fc",
      "description": "Unsupported Kubernetes version is detected",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-supported-versions"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "7e9e8073-3d8b-47a9-ad8a-4d2d6bc8b0cb",
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
