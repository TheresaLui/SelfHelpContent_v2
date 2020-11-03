<properties
    pageTitle="Hostname certificate rotation failed."
    description="Hostname certificate rotation failed."
    authors="apicore"
    ms.author="aoapicoreaft"
    articleId="b882dd44-9d01-4d63-917b-1860dcfd1f01_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
	  ownershipId="Compute_APIManagement"
/>
# The following ADX clusters are not being used and are candidates for deletion.
---
{
  "recommendationOfferingId": "7e1fb574-eb4a-45d7-8db2-c85445aac53f",
  "recommendationOfferingName": "Azure API Management",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "8962964c-a6d6-4c3d-918a-2777f7fbdca7",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.ApiManagement/service",
  "recommendationFriendlyName": "HostnameCertRotationFail",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "apicore@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/apimanage/serviceloop",
      "service": "API Management",
      "team": "ServicingLoop"
    },
    "serviceTreeId": "6ba70dfa-ead9-4cc1-b894-049f8a17c22b"
  },
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/api-management/configure-custom-domain",
  "description": "Hostname certificate rotation failed",
  "longDescription": "API Management service failed to refresh hostname certificate from Key Vault. Please ensure that certificate exists in Key Vault and API Management service identity is granted read access.",
  "potentialBenefits": "Ensure service availability",
  "displayLabel": "Hostname certificate rotation failed",
  "additionalColumns": [
    {
      "name": "message",
      "title": "Message"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "72430dca-3844-4a48-8e6c-8711df8e0e6f",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "actions": [
    {
      "actionId": "597a9ec5-5178-44c2-ba8d-e298a3fa4e5a",
      "description": "Manage hostnames",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "apim-hostname"
      }
    }
  ],
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://apim.kusto.windows.net').database('APIMProd').AzureAdvisor_HostnameCertificateRotationFailed",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  }
}
---
