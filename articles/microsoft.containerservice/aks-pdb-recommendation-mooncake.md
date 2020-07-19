<properties
    pageTitle="Pod Disruption Budgets Recommended"
    description="Pod Disruption Budgets Recommended"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="6fdf4656-d8b1-465d-9fb5-864379ffecfd"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="Compute_AzureKubernetesService"
/>

# Pod Disruption Budgets Recommended
---
{
  "recommendationOfferingId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "cbd1b299-b933-45bb-83a5-4061e515e826",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('akscn.kusto.chinacloudapi.cn').database('AKSprod').PDBRecommendation",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.ContainerService/managedClusters",
  "recommendationFriendlyName": "PodDisruptionBudgetsRecommended",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "potentialBenefits": "Improve service high availability",
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
  "description": "Pod Disruption Budgets Recommended",
  "longDescription": "Pod Disruption Budgets Recommended. Improve service high availability.",
  "actions": [
    {
      "actionId": "3cb8cdc3-fd20-4d0a-b467-356c3b8a602c",
      "description": "Pod Disruption Budgets Recommended",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-pdb"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "41c18c25-b9da-45c8-b767-0c198b2f4066",
    "actionType": "Blade",
    "bladeName": "ResourceMenuBlade",
    "extensionName": "HubsExtension",
    "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Pod Disruption Budgets Recommended",
  "additionalColumns": [],
  "learnMoreLink": "https://aka.ms/aks-pdb"
}
---
