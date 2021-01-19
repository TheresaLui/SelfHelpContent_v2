<properties
    pageTitle="Upgrade SDK version recommendation"
    description="Return list of resources that do not currently use the recommended SDK version"
    ms.author="osmuller"
    articleId="89df03c6-017c-4061-bc7e-f33e772339d0_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="public,usnat,ussec"
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
		"streamNamespace": "cluster('https://keyvault.kusto.windows.net').database('warm-public').GetAzureAdvisorRecommendedSdkReport",
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
