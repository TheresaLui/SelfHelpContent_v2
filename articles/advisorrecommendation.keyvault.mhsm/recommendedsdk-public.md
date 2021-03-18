<properties
    pageTitle="Upgrade SDK version recommendation"
    description="Return list of resources that do not currently use the recommended SDK version"
    ms.author="mhsmdevs"
    articleId="3a4f2678-d73a-4076-bacb-dc6a9221f3b5_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="public,usnat,ussec"
    ownershipId="AzureKeyVault_MHSM"
/>
# Key Vault SDK Version Recommendation
---
{
	"recommendationOfferingId": "8e93a1fd-5378-4ec7-a1e7-135f74745054",
	"recommendationOfferingName": "Key Vault",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "47e36ece-24bb-4d3e-8172-af28c9df172d",
	"dataSourceMetadata": {
		"streamNamespace": "cluster('https://azuremanagedhsmprod.kusto.windows.net').database('azuremanagedhsmprod').GetAzureAdvisorRecommendedSdkReport",
		"dataSource": "Kusto",
		"refreshInterval": "1.00:00:00"
	},
	"recommendationCategory": "Performance",
	"recommendationImpact": "Medium",
	"recommendationResourceType": "Microsoft.KeyVault/managedHsms",
	"recommendationFriendlyName": "UpgradeKeyVaultMHSMSDK",
	"recommendationMetadataState": "Active",
	"owner": {
		"email": "mhsmdevs@microsoft.com",
		"icm": {
			"routingId": "ADROCS://Recovery/AzureManagedHSMProd",
			"service": "Azure Managed HSM",
			"team": "Triage"
		},
		"serviceTreeId": "2673daf5-683b-4f60-aa7b-d0313ecf4e70"
	},
	"version": 2,
	"learnMoreLink": "https://docs.microsoft.com/azure/key-vault/general/client-libraries",
	"description": "Update Key Vault SDK Version",
	"longDescription": "New Key Vault Client Libraries are split to keys, secrets, and certificates SDKs, which are integrated with recommended Azure Identity library to provide seamless authentication to Key Vault across all languages and environments. It also contains several performance fixes to issues reported by customers and proactively identified through our QA process.
	Important: Please be aware that you can only remediate recommendation for custom applications you have access to. Recommendations can be shown due to integration with other Azure services like Storage, Disk encryption, which are in process to update to new version of our SDK. If you use .NET 4.0 in all your applications please dismiss",
	"potentialBenefits": "Latest Key Vault Client Libraries contain fixes for known issues and additional improvements.",
	"supportedSDKLanguages": [".Net", "Python", "Node.js"],
	"actions": [{
			"actionId": "46f46aa2-1549-4bba-bb61-09d311774720",
			"description": "Learn how to update your Key Vault Client Libraries",
			"actionType": "Document",
			"documentLink": "{recommendedActionLearnMore}"
		},
		{
			"actionId": "46f46aa2-1549-4bba-bb61-09d311774721",
			"description": "View {version} release notes",
			"actionType": "Document",
			"documentLink": "{releaseNotes}"
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "46f46aa2-1549-4bba-bb61-09d311774722",
			"actionType": "Blade",
			"extensionName": "Microsoft_Azure_KeyVault",
			"bladeName": "VaultBlade",
			"metadata": {
				"id": "{resourceId}"
			}
		}
	},
	"displayLabel": "Update Key Vault Library",
	"additionalColumns": [
		{
			"name": "lan",
			"title": "Detected language"
		},
		{
			"name": "sdk",
			"title": "Detected SDK"
		},
		{
			"name": "currentVersion",
			"title": "Detected version"
		}
	],
	"tip": ""
}
---
