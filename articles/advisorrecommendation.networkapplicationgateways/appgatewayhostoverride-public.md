<properties
    pageTitle="Do not override hostname to ensure website integrity"
    description="Do not override hostname to ensure website integrity"
    authors="christoc"
    ms.author="christoc"
    articleId="52a9d0a7-efe1-4512-9716-394abd4e0ab1_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>
# Avoid hostname override to ensure site integrity
---
{
  "recommendationOfferingId": "95028b6a-341d-461d-bffd-f83b7eddf59f",
  "recommendationOfferingName": "Application Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "52a9d0a7-efe1-4512-9716-394abd4e0ab1",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hybridnetworking.kusto.windows.net').database('GatewayManager').appgwAdvisorRecommendationForHostNameOverride",
    "dataSource": "Kusto",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/applicationGateways",
  "recommendationFriendlyName": "AppGatewayHostOverride",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "appgwpm@microsoft.com",
    "icm": {
      "routingId": "adrocs://Recovery/AppGWT",
      "service": "Azure Application Gateway",
      "team": "Azure Application Gateway"
    },
    "serviceTreeId": "95028b6a-341d-461d-bffd-f83b7eddf59f"
  },
  "ingestionClientIdentities": [],
  "version": 3.0,
  "learnMoreLink": "https://aka.ms/appgw-advisor-usecustomdomain",
  "description": "Avoid hostname override to ensure site integrity",
  "longDescription": "Try to avoid overriding the hostname when configuring Application Gateway.  Having a different domain on the frontend of Application Gateway than the one which is used to access the backend can potentially lead to cookies or redirect urls being broken.  Note that this might not be the case in all situations and that certain categories of backends (like REST API's) in general are less sensitive to this.  Please make sure the backend is able to deal with this or update the Application Gateway configuration so the hostname does not need to be overwritten towards the backend.  When used with App Service, attach a custom domain name to the Web App and avoid use of the *.azurewebsites.net host name towards the backend.",
  "potentialBenefits": "Ensure site integrity and avoid broken cookies or redirect urls through a resilient Application Gateway configuration.",
  "actions": [
    {
      "actionId": "052c8a91-52d7-4109-bcc2-7ee52b21bed3",
      "description": "Inspect the Application Gateway Http Settings",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_HybridNetworking",
      "bladeName": "ApplicationGatewayHttpSettingsGridBlade",
       "metadata": {
        "id": "{resourceId}",
        "menuid": "httpsettings"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "cf8b82b2-8588-4d53-bdbd-9b178671c9d4",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_HybridNetworking",
      "bladeName": "ApplicationGatewayBladeV2",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Do not override hostname to ensure website integrity",
  "additionalColumns": [{ "name": "RulesInViolation", "title": "Rules" }]
}
---
