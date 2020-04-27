<properties
    pageTitle="Update AKS Service Principal"
    description="Update AKS Service Principal"
    authors="jakepearson"
    ms.author="jopears"
    articleId="f1b8daef-d5f7-443d-ba7a-fa4f072829a4"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
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
    "streamNamespace": "cluster('aksff.kusto.usgovcloudapi.net').database('AKSprod').ServicePrincipalExpired",
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
      "actionId": "f32698fe-919f-4f57-9dc0-287fcf41cf75",
      "description": "Update Service Principal",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/aks/update-credentials"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "02491432-be79-4a6d-abd8-209a097e207c",
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
