<properties
    pageTitle="Deprecated Kubernetes API in 1.16 is found"
    description="Deprecated Kubernetes API in 1.16 is found"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="10800c39-fc11-4c42-9d42-fd31a58965a1"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="Compute_AzureKubernetesService"
/>

# Deprecated Kubernetes API in 1.16 is found
---
{
  "recommendationOfferingId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "01e2919e-3693-44b7-861b-a6d20f65d4af",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('aksff.kusto.usgovcloudapi.net').database('AKSprod').DeprecatedKubernetesAPI116",
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
      "actionId": "039f41c5-0b65-4dee-9c4e-0e955a16215b",
      "description": "Deprecated Kubernetes API in 1.16 is found",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-deprecated-k8s-api-1.16"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "06222734-2980-4c78-ab7b-cf523b27bb4d",
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
