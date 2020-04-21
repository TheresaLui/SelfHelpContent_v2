<properties
    pageTitle="Monitoring addon workspace is deleted"
    description="Monitoring addon workspace is deleted"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="2edde431-0bff-427f-812a-dc4498753be6"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="Compute_AzureKubernetesService"
/>

# Monitoring addon workspace is deleted
---
{
  "recommendationOfferingId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "4a675efc-039f-4953-917c-7580ea7aa955",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('aksff.kusto.usgovcloudapi.net').database('AKSprod').OmsWorkspaceDeleted",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.ContainerService/managedClusters",
  "recommendationFriendlyName": "MonitoringAddonWorkspaceIsDeleted",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "potentialBenefits": "Correct issues to setup monitoring addon",
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
  "description": "Monitoring addon workspace is deleted",
  "longDescription": "Monitoring addon workspace is deleted. Correct issues to setup monitoring addon.",
  "actions": [
    {
      "actionId": "663e60fd-0ffd-45f4-92b6-c38597bf7c98",
      "description": "Monitoring addon workspace is deleted",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-disable-monitoring-addon"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "ee852201-45b5-485d-bb32-dc6bb165a838",
    "actionType": "Blade",
    "bladeName": "ResourceMenuBlade",
    "extensionName": "HubsExtension",
    "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Monitoring addon workspace is deleted",
  "additionalColumns": [],
  "learnMoreLink": "https://aka.ms/aks-disable-monitoring-addon"
}
---
