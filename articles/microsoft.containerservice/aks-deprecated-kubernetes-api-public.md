<properties
    pageTitle="Deprecated Kubernetes API in 1.16 is found"
    description="Deprecated Kubernetes API in 1.16 is found"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="458b3db2-e361-4f7f-95b2-71065a57645a"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="Compute_AzureKubernetesService"
/>

# Deprecated Kubernetes API in 1.16 is found
---
{
  "recommendationOfferingId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "b4704ab8-e8fd-4bb4-8096-d04b073ede2d",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('aks.kusto.windows.net').database('AKSprod').DeprecatedKubernetesAPI116",
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
      "actionId": "444dc7a9-67af-4193-bbb5-a03bcb6f7f39",
      "description": "Deprecated Kubernetes API in 1.16 is found",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-deprecated-k8s-api-1.16"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "c7d8d125-c575-45d8-b261-c1c6c4ca9848",
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
