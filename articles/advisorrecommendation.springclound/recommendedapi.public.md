<properties
    pageTitle="Upgrade API version recommendation"
    description="Return list of resources that do not currently use the recommended API version"
    authors="liping-ms"
    ms.author="springazure"
    articleId="c421d51c-fb47-4b8b-8630-0f067e033fa1_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="public,ussec,usnat"
    ownershipId="DevDivAzServices_SpringCloud"
/>


# Spring Cloud API Version Recommendation
---

{
   "recommendationOfferingId": "9cb52795-75ca-46f7-acc0-e3213428dc2c",
   "recommendationOfferingName": "Azure Spring Cloud",
   "$schema": "AdvisorRecommendation",
   "recommendationTypeId": "3c7ddb62-d514-4794-ba90-8ce5275a7a81",
   "dataSourceMetadata": {
      "streamNamespace": "cluster('https://springcloud.eastus2.kusto.windows.net').database('prod').GetAzureAdvisorRecommendationReport",
      "dataSource": "Kusto",
      "refreshInterval": "0.00:10:00"
   },
   "recommendationCategory": "Operational excellence",
   "recommendationImpact": "Medium",
   "recommendationResourceType": "Microsoft.AppPlatform/Spring",
   "recommendationFriendlyName": "UpgradeSpringCloudAPI",
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
   "version": 2.0,
   "learnMoreLink": "https://docs.microsoft.com/azure/spring-cloud",
   "description": "Update Azure Spring Cloud API Version",
   "longDescription": "We have identified API calls from outdated Azure Spring Cloud API for resources under this subscription. We recommend switching to the latest Spring Cloud API versions. You need to update your existing code to use the latest API version. Also, you need to upgrade your Azure SDK and Azure CLI to the latest version. This ensures you receive the latest features and performance improvements.",
   "potentialBenefits": "Latest Azure Spring Cloud API contain latest fixes, performance improvements, and new feature capabilities.",
   "supportedSDKLanguages": [".NET", "Java", "JavaScript/TypeScript", "Python", "C++", "Embedded C", "Android", "IOS"],
   "actions": [{
         "actionId": "9017e82f-b7ac-4a06-8b9b-5858cb3d5113",
         "description": "Upgrade your Azure Spring Cloud API",
         "actionType": "Document",
         "documentLink": "{recommendedActionLearnMore}"
      }
   ],
   "resourceMetadata": {
      "action": {
         "actionId": "54fd58dd-340f-463f-9c61-1f7bd08690b4",
         "actionType": "Blade",
         "extensionName": "Microsoft_Spring_Cloud",
         "bladeName": "ResourceOverviewBlade",
         "metadata": {
            "id": "{resourceId}"
         },
         "documentLink": ""
      }
   },
   "displayLabel": "Update Azure Spring Cloud API",
   "tip": ""
}
---
