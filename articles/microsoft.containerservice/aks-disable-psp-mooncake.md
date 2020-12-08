<properties
    pageTitle="Use Azure Policy instead of Pod Security Policy"
    description="Use Azure Policy instead of Pod Security Policy"
    authors="jomore"
    ms.author="jomore"
    articleId="ec043493-dc58-4f17-8686-2f60f50f1055_mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
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
    "streamNamespace": "cluster('akscn.kusto.chinacloudapi.cn').database('AKSprod').PodSecurityPolicyEnabled",
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
      "actionId": "e0c519d6-837c-48b0-84f0-11c2dc4ff817",
      "description": "Use Azure Policy for AKS instead of Pod Security Policies",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/aks/use-pod-security-on-azure-policy"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "642d255b-3f81-43a7-bc73-4eb8bd84040e",
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
