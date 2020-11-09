<properties
    pageTitle="Backup the Managed HSM Recommendation"
    description="Return list of Managed HSM resources that haven't been backup from in 30 days"
    ms.author="mhsmdevs"
    articleId="38e27ecb-504e-4395-8df7-1a60d1552102_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="public,usnat,ussec"
    ownershipId="AzureKeyVault_MHSM"
/>
# Managed HSM Backup Recommendation
---
{
	"recommendationOfferingId": "8e93a1fd-5378-4ec7-a1e7-135f74745054",
	"recommendationOfferingName": "Key Vault",
	"$schema": "AdvisorRecommendation",
	"recommendationTypeId": "41b42080-0c57-4840-b1ef-e04fdc6fe948",
	"dataSourceMetadata": {
		"streamNamespace": "cluster('https://azuremanagedhsmprod.kusto.windows.net').database('azuremanagedhsmprod').GetAzureAdvisorRecommendedBackupReport",
		"dataSource": "Kusto",
		"refreshInterval": "00:30:00"
	},
	"recommendationCategory": "OperationalExcellence",
	"recommendationImpact": "Medium",
	"recommendationResourceType": "Microsoft.KeyVault/managedHsms",
	"recommendationFriendlyName": "BackupKeyVaultMHSM",
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
	"version": 1,
	"learnMoreLink": "https://docs.microsoft.com/azure/key-vault/managed-hsm/best-practices",
	"description": "Your Managed HSM pool hasn't been backed-up in last 30 days",
	"longDescription": "It is a recommended operation best practice to backup your Managed HSM at least once every 30 days. This will protect your from lost of keys in case of catastrophic event",
	"potentialBenefits": "Improved data loss prevention",
	"actions": [{
			"actionId": "273dfffa-cbc3-48f4-bba3-df198bd7f487",
			"description": "Backup your Managed HSM pool now",
			"actionType": "Document",
			"documentLink": "https://docs.microsoft.com/azure/key-vault/managed-hsm/backup-restore"
		},
		{
			"actionId": "273dfffa-cbc3-48f4-bba3-df198bd7f488",
			"description": "View Best practices of Managed HSM",
			"actionType": "Document",
			"documentLink": "https://docs.microsoft.com/azure/key-vault/managed-hsm/best-practices"
		}
	],
	"resourceMetadata": {
		"action": {
			"actionId": "273dfffa-cbc3-48f4-bba3-df198bd7f489",
			"actionType": "Blade",
			"extensionName": "Microsoft_Azure_KeyVault",
			"bladeName": "VaultBlade",
			"metadata": {
				"id": "{resourceId}"
			}
		}
	},
	"displayLabel": "Your Managed HSM pool hasn't been backedup for last 30 days",
	"additionalColumns": [
		{
			"name": "PoolName",
			"title": "Pool Name"
		},
		{
			"name": "Remind",
			"title": "Last Time Backup Hint"
		}
	],
	"tip": ""
}
---
