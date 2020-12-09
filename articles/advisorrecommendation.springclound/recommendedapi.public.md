<properties
    pageTitle="Upgrade API version recommendation"
    description="Return list of resources that do not currently use the recommended API version"
	authors="liping-ms"
    ms.author="springazure"
	displayOrder="100"
    articleId="c421d51c-fb47-4b8b-8630-0f067e033fa1_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
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
		"streamNamespace": "cluster('https://springcloud.eastus2.kusto.windows.net').database('prod').GetApiVersionRecommendationReport",
		"dataSource": "Kusto",
		"refreshInterval": "0.12:00:00"
	},
	"recommendationCategory": "Performance",
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
	"version": 1,
	"learnMoreLink": "https://docs.microsoft.com/rest/api/azurespringclould",
	"description": "Update your current Azure Spring Cloud API version to the most recent version.",
	"longDescription": "We have identified rest calls from outdated Azure Spring Cloud Version for resources under this subscription. We recommend switching to the latest Azure Spring Cloud versions. You need to update your existing code or scripts to use the latest API version. This ensures you receive the latest security and performance improvements.",
	"potentialBenefits": "Improved security, performance, data resiliency, and support for new features.",
	"supportedSDKLanguages": [".Net"],
	"actions": [{
			"actionId": "9017e82f-b7ac-4a06-8b9b-5858cb3d5113",
			"description": "Learn how to update your Azure Spring Cloud API",
			"actionType": "Document",
			"documentLink": "{recommendedActionLearnMore}"
		},
		{
			"actionId": "01ee32f0-0aad-4da7-bc44-17eeee4dcea0",
			"description": "View {version} release notes",
			"actionType": "Document",
			"documentLink": "{releaseNotes}"
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "54fd58dd-340f-463f-9c61-1f7bd08690b4",
			"actionType": "Blade",
			"extensionName": "Microsoft_Spring_Cloud",
			"bladeName": "VaultBlade",
			"metadata": {
				"id": "{resourceId}"
			}
		}
	},
	"displayLabel": "Update Azure Spring Cloud API",
	"additionalColumns": [{
			"name": "language",
			"title": "SDK Language"
		},
		{
			"name": "version",
			"title": "Minimum Recommended Version"
		}
	],
	"tip": ""
}
---
