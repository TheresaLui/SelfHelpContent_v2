<properties
    pageTitle="Upgrade SDK version recommendation"
    description="Return list of resources that do not currently use the recommended SDK version"
	authors="liping-ms"
    ms.author="lipinggao"
    displayOrder="100"
    articleId="b72ddf41-39a2-4158-8492-11ec868aee98_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="DevDivAzServices_SpringCloud"
/>
# Spring Cloud SDK Version Recommendation
---
{
	"recommendationOfferingId": "997d7803-aa34-419e-8c09-d7cd8a4ceff2",
	"recommendationOfferingName": "Azure Spring Cloud",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "64f45690-9b55-457f-ba91-9c02353ffa2a",
	"dataSourceMetadata": {
		"streamNamespace": "cluster('https://lgacluster.westus.kusto.windows.net').database('lga-db').GetAzureAdvisorRecommendedSdkReport",
		"dataSource": "Kusto",
		"refreshInterval": "1.00:00:00"
	},
	"recommendationCategory": "Performance",
	"recommendationImpact": "Medium",
	"recommendationResourceType": "Microsoft.AppPlatform/Spring",
	"recommendationFriendlyName": "UpgradeStaleSDK",
	"recommendationMetadataState": "Active",
	"owner": {
		"email": "lipinggao@microsoft.com",
		"icm": {
			"routingId": "AZUREDISTRIBUTEDMANAGEDSERVICEFORSPRING\\AzDMSS-Triage",
			"service": "Azure Spring Cloud",
			"team": "Azure Spring Cloud"
		},
		"serviceTreeId": "997d7803-aa34-419e-8c09-d7cd8a4ceff2"
	},
	"version": 1,
	"learnMoreLink": "https://docs.microsoft.com/azure/key-vault/general/client-libraries",
	"description": "Update Spring Cloud SDK Version",
	"longDescription": "New Key Vault Client Libraries are split to keys, secrets, and certificates SDKs, which are integrated with recommended Azure Identity library to provide seamless authentication to Key Vault across all languages and environments. It also contains several performance fixes to issues reported by customers and proactively identified through our QA process.<br><br>**PLEASE DISMISS:**<br>If Key Vault is integrated with Azure Storage, Disk or other Azure services which can use old Key Vault SDK and when all your current custom applications are using .NET SDK 4.0 or above.",
	"potentialBenefits": "Latest Key Vault Client Libraries contain fixes for known issues and additional improvements.",
	"supportedSDKLanguages": [".Net"],
	"actions": [{
			"actionId": "9017e82f-b7ac-4a06-8b9b-5858cb3d5113",
			"description": "Learn how to update your Key Vault Client Libraries",
			"actionType": "Document",
			"documentLink": "{recommendedActionLearnMore}"
		},
		{
			"actionId": "9017e82f-b7ac-4a06-8b9b-5858cb3d5114",
			"description": "View {version} release notes",
			"actionType": "Document",
			"documentLink": "{releaseNotes}"
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "9017e82f-b7ac-4a06-8b9b-5858cb3d5115",
			"actionType": "Blade",
			"extensionName": "Microsoft_Azure_KeyVault",
			"bladeName": "VaultBlade",
			"metadata": {
				"id": "{resourceId}"
			}
		}
	},
	"displayLabel": "Update Key Vault Library",
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
