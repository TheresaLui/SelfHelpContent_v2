<properties
    pageTitle="Fix the backup database settings of your App Service resource"
    description="Fix the backup database settings of your App Service resource"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="b30897cc-2c2e-4677-a2a1-107ae982ff49_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
	ownershipId="Compute_AppService"
/>
# Fix the backup database settings of your App Service resource
---
{
  "recommendationOfferingId": "c7f69506-5b4f-4751-b423-0095e68fad64",
  "recommendationOfferingName": "App Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "b30897cc-2c2e-4677-a2a1-107ae982ff49",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Web/sites",
  "recommendationFriendlyName": "AppServiceFixBackupDatabaseSettings",
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
  "bfc9fa96-6f4a-42b3-894f-29ff56b2bc89"
  ],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/antbc_cn",
  "description": "Fix the backup database settings of your App Service resource",
  "longDescription": "Your app's backups are consistently failing due to invalid DB configuration, you can find more details in backup history.",
  "potentialBenefits": "Ensure business continuity",
  "actions": [
    {
      "actionId": "70901239-4FCA-4F1B-AE0E-E6ED506869F5",
      "description": "Go to backup settings",
      "actionType": "Blade",
      "extensionName": "WebsitesExtension",
      "bladeName": "backupSummaryBlade",
       "metadata": {
        "resourceUri": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "0E98084D-B10D-4070-8022-2D737C7A4072",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Fix backup database settings"
}
---
