<properties
    pageTitle="Update AKS Service Principal"
    description="Update AKS Service Principal"
    authors="jakepearson"
    ms.author="jopears"
    articleId="58a6b6c6-7653-4d7d-8d89-3d71f04fc010"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
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
    "streamNamespace": "cluster('akscn.kusto.chinacloudapi.cn').database('AKSprod').ServicePrincipalExpired",
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
      "actionId": "2cdb95ff-69de-4309-9fde-c9bcb52b0f01",
      "description": "Update Service Principal",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/aks/update-credentials"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "78e13004-c5c3-4f1c-87a3-195ffc4bf7da",
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
