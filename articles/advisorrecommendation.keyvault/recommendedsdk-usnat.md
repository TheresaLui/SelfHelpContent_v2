<properties
    pageTitle="Upgrade SDK version recommendation"
    description="Return list of resources that do not currently use the recommended SDK version"
    ms.author="osmuller"
    articleId="89df03c6-017c-4061-bc7e-f33e772339d0_usnat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="usnat"
    ownershipId="AzureKeyVault_KeyVault"
/>
# Key Vault SDK Version Recommendation
---
{
	"recommendationOfferingId": "8e93a1fd-5378-4ec7-a1e7-135f74745054",
	"recommendationOfferingName": "KeyVault",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "9017e82f-b7ac-4a06-8b9b-5858cb3d5113",
	"dataSourceMetadata": {
		"streamNamespace": "cluster('https://keyvaultex.usnateast.kusto.core.eaglex.ic.gov').database('warm').GetAzureAdvisorRecommendedSdkReport",
		"dataSource": "Kusto",
		"refreshInterval": "1.00:00:00"
	},
	"recommendationCategory": "Performance",
	"recommendationImpact": "Medium",
	"recommendationResourceType": "Microsoft.KeyVault/vaults",
	"recommendationFriendlyName": "UpgradeKeyVaultSDK",
	"recommendationMetadataState": "Active",
	"owner": {
		"email": "azkvicm@microsoft.com",
		"icm": {
			"routingId": "adrocs://Recovery/AzKV",
			"service": "Azure Key Vault",
			"team": "Triage"
		},
		"serviceTreeId": "51c86b53-37ee-4e99-9747-89d133719ac4"
	},
	"version": 1,
	"learnMoreLink": "https://docs.microsoft.com/azure/key-vault/general/client-libraries",
	"description": "Update Key Vault SDK Version",
	"longDescription": "The latest version of Key Vault Client Libraries contains fixes to issues reported by customers and proactively identified through our QA process.",
	"potentialBenefits": "Latest Key Vault Client Libraries contain fixes for known issues and additional improvements.",
	"supportedSDKLanguages": [".Net","ManagementPlaneSdk"],
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