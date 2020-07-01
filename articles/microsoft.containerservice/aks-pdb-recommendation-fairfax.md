<properties
    pageTitle="Pod Disruption Budgets Recommended"
    description="Pod Disruption Budgets Recommended"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="adfbfb45-0b4d-4d6d-96b5-bc458ae07a3a"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
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
    "streamNamespace": "cluster('aksff.kusto.usgovcloudapi.net').database('AKSprod').PDBRecommendation",
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
      "actionId": "8076078c-f46a-4e07-b4d3-cde5a637adf0",
      "description": "Pod Disruption Budgets Recommended",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-pdb"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "d87045b7-9e82-498d-bf7a-d6c38b5eed52",
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
