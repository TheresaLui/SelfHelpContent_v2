<properties
    pageTitle="Connect to Azure Synapse workspace using private links"
    description="Connect to Azure Synapse workspace using private links"
    authors="srthatip"
    ms.author="srthatip"
    articleId="ae4bc204-d780-494c-aa61-dbd46f403315_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_AzureSQLDB_DataWarehouse"
/>

# Consider deleting firewall rules and connect to Azure Synapse workspace using private links
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "Azure Synapse Analytics",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "ae4bc204-d780-494c-aa61-dbd46f403315",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('analytics365prod.kusto.windows.net').database('Analytics365PROD').synapse_advisor_ConnectUsingPrivateLinks",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Security",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Synapse/workspaces",
  "recommendationFriendlyName": "SynapseWorkspaceConnectUsingPrivateLinks",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "a365rp@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/AzureSynapsePlateform/SynapseProvider",
      "service": "Azure Synapse Platform Service",
      "team": "Synapse Resource Provider"
    },
    "serviceTreeId": "c0ee70d5-102d-438c-8858-795b92dc0f99"
  },
  "ingestionClientIdentities": [ ],
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-private-endpoints",
  "description": "Consider deleting firewall rules and connect to Azure Synapse workspace using private links",
  "longDescription": "Managed private endpoints are private endpoints created in the Managed workspace Microsoft Azure Virtual Network establishing a private link to Azure resources. Azure Synapse manages these private endpoints on your behalf. When you use a private link, traffic between your Virtual Network and workspace traverses entirely over the Microsoft backbone network. Private Link protects against data exfiltration risks. You establish a private link to a resource by creating a private endpoint.",
  "potentialBenefits": "Private endpoint uses a private IP address from your Virtual Network to effectively bring the service into your Virtual Network. Private endpoints are mapped to a specific resource in Azure and not the entire service. Customers can limit connectivity to a specific resource approved by their organization.",
  "actions": [
    {
      "actionId": "de8794d0-4f6a-4722-9a32-dcb89f3cd4ab",
      "description": "Consider deleting firewall rules and connect to Azure Synapse workspace using private links",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-private-endpoints"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "52ac99d6-8b81-4bdb-ad63-86cf6984d5ff",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Consider deleting firewall rules and connect to Azure Synapse workspace using private links",
  "additionalColumns": [],
  "tip": "Consider deleting firewall rules and connect to Azure Synapse workspace using private links."

}
---
