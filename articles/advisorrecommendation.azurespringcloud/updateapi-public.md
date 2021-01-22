<properties
    pageTitle="Upgrade API version recommendation"
    description="Return list of resources that do not currently use the recommended API version"
    authors="liping-ms"
    ms.author="springazure"
    articleId="1d368336-771c-4a88-b2d9-4bb0225ed4e5_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="public,ussec,usnat"
    ownershipId="DevDivAzServices_SpringCloud"
/>


# Spring Cloud API Version Recommendation
---

{
   "recommendationOfferingId": "68179c28-1999-4491-9657-14a5084fe4a5",
   "recommendationOfferingName": "Azure Spring Cloud",
   "$schema": "AdvisorRecommendation",
   "recommendationTypeId": "7c3484ae-c299-46d0-912d-d77aaeb1feb7",
   "dataSourceMetadata": {
      "streamNamespace": "cluster('https://springcloud.eastus2.kusto.windows.net').database('prod').GetAzureAdvisorRecommendationReport",
      "dataSource": "Kusto",
      "refreshInterval": "0.12:00:00"
   },
   "recommendationCategory": "OperationalExcellence",
   "recommendationImpact": "Medium",
   "recommendationResourceType": "Microsoft.AppPlatform/Spring",
   "recommendationFriendlyName": "UpgradeAzureSpringCloudAPI",
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
   "longDescription": "We have identified API calls from outdated Azure Spring Cloud API for resources under this subscription. We recommend switching to the latest Spring Cloud API version. You need to update your existing code to use the latest API version. Also, you need to upgrade your Azure SDK and Azure CLI to the latest version. This ensures you receive the latest features and performance improvements.",
   "potentialBenefits": "Latest Azure Spring Cloud API contains latest fixes, performance improvements, and new feature capabilities.",
   "actions": [{
         "actionId": "9017e82f-b7ac-4a06-8b9b-5858cb3d5113",
         "description": "Upgrade to version 2020-07-01",
         "actionType": "Document",
         "documentLink": "https://docs.microsoft.com/cli/azure/ext/spring-cloud/?view=azure-cli-latest"
      }
   ],
   "resourceMetadata": {
   "action": {
      "actionId": "526a0a32-97c9-4132-9cef-e39140985e25",
      "actionType": "Blade",
      "extensionName": "AppPlatformExtension",
      "bladeName": "ResourceOverviewBlade",
      "metadata": {
         "id": "{resourceId}"
         }
      }
   },
   "displayLabel": "Update Azure Spring Cloud API",
   "tip": ""
}
---
