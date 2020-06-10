<properties
    pageTitle="Update AKS Service Principal"
    description="Update AKS Service Principal"
    authors="jakepearson"
    ms.author="jopears"
    articleId="5ed99507-3d01-49cf-8ddd-0984de5a624d"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="Compute_AzureKubernetesService"
/>

# Update AKS Service Principal 
---
{
  "recommendationOfferingId": "4c4a2d61-b806-47af-a7ee-e8f8fcfce8bb",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "4c72c554-1573-4ce8-8bbf-7b2aab0bf297",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('aks.kusto.windows.net').database('AKSprod').ServicePrincipalExpired",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.ContainerService/managedClusters",
  "recommendationFriendlyName": "UpdateServicePrincipal",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "potentialBenefits": "Your cluster will work correctly",
  "owner": {
    "email": "jopears@microsoft.com",
    "icm": {
      "routingId": "MDM://ACSRP",
      "service": "Azure Kubernetes Service",
      "team": "Azure Kubernetes Service"
    },
    "serviceTreeId": "c77cbc0e-e61d-4aa0-9672-b63d529eac77"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "description": "Update cluster's service principal",
  "longDescription": "This cluster's service principal is expired and the cluster will not be healthy until the service principal is updated",
  "actions": [
    {
      "actionId": "9daffb0d-5a5a-4c13-9fba-5153733c6788",
      "description": "Update Service Principal",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/aks/update-credentials"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "6646a29d-5714-4c9a-a226-9ea94fc1de8a",
    "actionType": "Blade",
    "bladeName": "ResourceMenuBlade",
    "extensionName": "HubsExtension",
    "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Update Service Principal",
  "additionalColumns": [],
  "learnMoreLink": "https://docs.microsoft.com/azure/aks/update-credentials"
}
---
