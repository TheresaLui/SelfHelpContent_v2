<properties
    pageTitle="Use Azure Policy instead of Pod Security Policy"
    description="Use Azure Policy instead of Pod Security Policy"
    authors="jomore"
    ms.author="jomore"
    articleId="54439cca-37cf-4471-a350-4ed99414efa4_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
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
    "streamNamespace": "cluster('aks.kusto.windows.net').database('AKSprod').PodSecurityPolicyEnabled",
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
    "serviceTreeId": "a3635587-7815-493b-83a2-ae0def4bf2f5"
  },
  "ingestionClientIdentities": [],
  "version": 1.1,
  "description": "Disable the Application Routing Addon",
  "longDescription": "This cluster has Pod Security Policies enabled, which are going to be deprecated in favor of Azure Policy for AKS",
  "actions": [
    {
      "actionId": "537d1199-98b6-4ed9-8199-71339180fed3",
      "description": "Use Azure Policy for AKS instead of Pod Security Policies",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/aks/use-pod-security-on-azure-policy"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "1f87d2f9-9d8e-428d-ada9-be707e11fceb",
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
