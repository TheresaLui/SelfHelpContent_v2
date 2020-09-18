<properties
    pageTitle="Monitoring addon workspace is deleted"
    description="Monitoring addon workspace is deleted"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="5a213a41-f5b3-4a8b-ba36-560147f6bbf3"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="Compute_AzureKubernetesService"
/>

# Monitoring addon workspace is deleted
---
{
  "recommendationOfferingId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "9ab7f49a-5b9e-4572-9a77-3fb73e60ecf4",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('akscn.kusto.chinacloudapi.cn').database('AKSprod').OmsWorkspaceDeleted",
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
      "actionId": "7bc47c22-91c6-4260-b410-199795c364ee",
      "description": "Monitoring addon workspace is deleted",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-disable-monitoring-addon"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "3d2b1a7e-85f9-44d1-9e1b-da94cbfcc880",
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
