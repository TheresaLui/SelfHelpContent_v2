<properties
    pageTitle="Monitoring addon workspace is deleted"
    description="Monitoring addon workspace is deleted"
    authors="JunSun17"
    ms.author="aksoverlay"
    articleId="cd23e33b-530c-4759-89af-f17e9ebd264b_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="Compute_AzureKubernetesService"
/>

# Monitoring addon workspace is deleted
---
{
  "recommendationOfferingId": "f1d1800e-d38e-41f2-b63c-72d59ecaf9c0",
  "recommendationOfferingName": "Azure Kubernetes Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "eedc2853-3369-4ede-8a75-68caf73e24df",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('aks.kusto.windows.net').database('AKSprod').OmsWorkspaceDeleted",
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
      "actionId": "6b4b4e3c-c81b-4c31-88f6-5c241583009f",
      "description": "Monitoring addon workspace is deleted",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aks-disable-monitoring-addon"
    }
  ],
  "resourceMetadata": {
    "action": {
    "actionId": "194fe03a-1f8f-43b3-bd02-6dcc5724921e",
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
