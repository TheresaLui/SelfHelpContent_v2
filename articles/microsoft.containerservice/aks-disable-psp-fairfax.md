<properties
    pageTitle="Use Azure Policy instead of Pod Security Policy"
    description="Use Azure Policy instead of Pod Security Policy"
    authors="jomore"
    ms.author="jomore"
    articleId="e3c328d9-184b-4699-9a15-18fa2d8cb30a_fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="Compute_AzureKubernetesService"
/>

# Disable PSP
---
{
  "recommendationOfferingId": "efaca250-af83-4cbe-b64d-8be83d79de83",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a347b531-5dbf-4870-80b0-ace7964605b1",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('aksff.kusto.usgovcloudapi.net').database('AKSprod').PodSecurityPolicyEnabled",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.ContainerService/managedClusters",
  "recommendationFriendlyName": "Use Azure Policy for Kubernetes",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "potentialBenefits": "AKS Pod Security Policies will be deprecated and Azure Policy for AKS should be used instead",
  "owner": {
    "email": "jomore@microsoft.com",
    "icm": {
      "routingId": "MDM://ACSRP",
      "service": "Azure Kubernetes Service",
      "team": "Azure Kubernetes Service"
    },
    "serviceTreeId": "efaca250-af83-4cbe-b64d-8be83d79de83"
  },
  "ingestionClientIdentities": [],
  "version": 1.1,
  "description": "Disable the Application Routing Addon",
  "longDescription": "This cluster has Pod Security Policies enabled, which are going to be deprecated in favor of Azure Policy for AKS",
  "actions": [
    {
      "actionId": "4232d663-6be7-4031-9973-90349501a2f9",
      "description": "Use Azure Policy for AKS instead of Pod Security Policies",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/aks/use-pod-security-on-azure-policy"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "0ffd7a7e-f690-4a9a-aacb-3efee832aceb",
      "actionType": "Blade",
      "bladeName": "ResourceMenuBlade",
      "extensionName": "HubsExtension",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Use Azure Policy for AKS instead of Pod Security Policies",
  "additionalColumns": [],
  "learnMoreLink": "https://docs.microsoft.com/azure/aks/use-pod-security-on-azure-policy"
}
---
