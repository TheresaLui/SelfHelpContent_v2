<properties
    pageTitle="Upgrade your outdated Azure Spring Cloud SDK to the latest version"
    description="Upgrade your outdated Azure Spring Cloud SDK to the latest version"
    authors="liping-ms"
    ms.author="springazure"
    articleId="37e2d85d-27d3-494b-bdd0-ddb1d7697c91_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="public,ussec,usnat"
    ownershipId="DevDivAzServices_SpringCloud"
/>

# Upgrade your outdated Azure Spring Cloud SDK to the latest version

---

{
  "recommendationOfferingId": "dfd38114-17bc-462c-bef7-73e283057e17",
  "recommendationOfferingName": "Azure Spring Cloud",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a0b3b756-caef-4f1c-9546-576e9f4cc7da",
  "dataSourceMetadata": {
     "streamNamespace": "cluster('https://springcloud.eastus2.kusto.windows.net').database('prod').GetSDKRecomendationReport",
     "dataSource": "Kusto",
     "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.AppPlatform/Spring",
  "recommendationFriendlyName": "SpringCloudUpgradeOutdatedSDK",
  "recommendationMetadataState": "Active",
  "owner": {
     "email": "springazure@microsoft.com",
     "icm": {
        "routingId": "AZUREDISTRIBUTEDMANAGEDSERVICEFORSPRING\\AzDMSS-Triage",
        "service": "Azure Spring Cloud",
        "team": "Azure Spring Cloud"
     },
     "serviceTreeId": "997d7803-aa34-419e-8c09-d7cd8a4ceff2"
  },
  "version": 3.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/spring-cloud",
  "description": "Update your outdated Azure Spring Cloud SDK to the latest version",
  "longDescription": "We have identified API calls from an outdated Azure Spring Cloud SDK. We recommend upgrading to the latest version for the latest fixes, performance improvements, and new feature capabilities.",
  "potentialBenefits": "Improve reliability, performance, and new feature capabilites.",
  "displayLabel": "Upgrade your outdated Azure Spring Cloud SDK to the latest version",
  "supportedSDKLanguages": ["Python", "Java", "Go", ".NET", "Node.js"],
  "additionalColumns": [
    {
      "name": "language",
      "title": "SDK Language"
    },
    {
      "name": "currentVersion",
      "title": "Current Version"
    },
    {
      "name": "version",
      "title": "Recommended Version"
    }
  ],
  "actions": [{
     "actionId": "9bc8335f-9656-4d29-bbf5-3517dd4ff318",
     "description": "Upgrade your {language} SDK",
     "actionType": "Document",
     "documentLink": "{recommendedActionLearnMore}"
     }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "93314dcf-73a8-4c89-8724-fed2fa3bc865",
      "actionType": "Blade",
      "extensionName": "AppPlatformExtension",
      "bladeName": "ResourceOverviewBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  }
}
---
