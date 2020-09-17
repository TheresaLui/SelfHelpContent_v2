<properties
    pageTitle="Fix the backup storage settings of your App Service resource"
    description="Fix the backup storage settings of your App Service resource"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="80efd6cb-dcee-491b-83a4-7956e9e058d5_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
	ownershipId="Compute_AppService"
/>
# Fix the backup storage settings of your App Service resource
---
{
  "recommendationOfferingId": "c7f69506-5b4f-4751-b423-0095e68fad64",
  "recommendationOfferingName": "App Service",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "80efd6cb-dcee-491b-83a4-7956e9e058d5",
  "dataSourceMetadata": {
    "dataSource": "SAS"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Web/sites",
  "recommendationFriendlyName": "AppServiceFixBackupStorageSettings",
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
  "description": "Fix the backup storage settings of your App Service resource",
  "longDescription": "Your app's backups are consistently failing due to invalid storage settings, you can find more details in backup history.",
  "potentialBenefits": "Ensure business continuity",
  "actions": [
    {
      "actionId": "241E74B8-FDFF-462A-B7CD-C5FE9FA9026E",
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
      "actionId": "842AAF30-15B0-4F45-80B4-4E73AEF09AC6",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Fix backup storage settings"
}
---
