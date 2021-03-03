<properties
    pageTitle="Pod Disruption Budgets Recommended"
    description="Pod Disruption Budgets Recommended"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="9738c5a0-a330-4465-a7f4-9132e004bd30_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
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
    "streamNamespace": "cluster('aks.kusto.windows.net').database('AKSprod').PDBRecommendation",
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
      "actionId": "278b8231-fb4a-4661-a6cd-b113288e0dd6",
      "description": "Pod Disruption Budgets Recommended",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-pdb"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "6fb5ee41-3423-4549-a31e-fc07076994e6",
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
