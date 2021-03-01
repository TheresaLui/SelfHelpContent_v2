<properties
    pageTitle="Hostname certificate rotation failed."
    description="Hostname certificate rotation failed."
    authors="apicore"
    ms.author="aoapicoreaft"
    articleId="f7725c0f-705b-4a97-86f7-7ce1b7a9de27_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	  ownershipId="Compute_APIManagement"
/>
# Following hostname certificates failed to rotate in AKV
---
{
  "recommendationOfferingId": "06ddf9f7-9c57-4d4e-b7eb-2682d9a91d8b",
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
  "learnMoreLink": "https://aka.ms/apimdocs/customdomain",
  "description": "Hostname certificate rotation failed",
  "longDescription": "API Management service failed to refresh hostname certificate from Key Vault. Ensure that certificate exists in Key Vault and API Management service identity is granted secret read access. Otherwise, API Management service will not be able to retrieve certificate updates from Key Vault, which may lead to the service using stale certificate and runtime API traffic being blocked as a result.",
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
    "streamNamespace": "cluster('https://apimchina.kusto.chinacloudapi.cn').database('APIMChina').AzureAdvisor_HostnameCertificateRotationFailed",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  }
}
---
