<properties
    pageTitle="Move your App Service Plan to PremiumV2 for better performance"
    description="Move your App Service Plan to PremiumV2 for better performance"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="9ebff5d5-10c1-4fed-8c58-1954e27d3bfa_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="Compute_AppService"
/>
# Move your App Service Plan to PremiumV2 for better performance
---
{
  "recommendationOfferingId": "c7f69506-5b4f-4751-b423-0095e68fad64",
  "recommendationOfferingName": "App Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "9ebff5d5-10c1-4fed-8c58-1954e27d3bfa",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Web/sites",
  "recommendationFriendlyName": "AppServiceMoveToPremiumV2",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "antgrowth@microsoft.com",
    "icm": {
      "routingId": "AIMS://ANTST",
      "service": "App Service",
      "team": "antrec"
    },
    "serviceTreeId": "df36aee8-c644-400b-a0ab-fd0f1191211d"
  },
  "ingestionClientIdentities": [
  "484db53f-83ae-4f6a-a922-931561863edb"
  ],
  "version": 1.1,
  "learnMoreLink": "https://aka.ms/ant-premiumv2_ff",
  "description": "Move your App Service Plan to PremiumV2 for better performance",
  "longDescription": "Your app served more than 1000 requests per day for the past 3 days. Your app may benefit from the higher performance infrastructure available with the Premium V2 App Service tier. The Premium V2 tier features Dv2-series VMs with faster processors, SSD storage, and doubled memory-to-core ratio when compared to the previous instances. Learn more about upgrading to Premium V2 from our documentation.",
  "potentialBenefits": "Obtain better performance with lower cost",
  "actions": [
    {
      "actionId": "28D57485-8B88-4B1E-8C43-09145ECDBA04",
      "description": "Move to Premium V2",
      "actionType": "Blade",
      "extensionName": "WebsitesExtension",
      "bladeName": "SpecPickerFrameBlade",
       "metadata": {
        "id": "{serverFarmId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "F71EDE4E-A61A-4B94-A565-7C44ED6591AB",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Try PremiumV2 SKU"
}
---
