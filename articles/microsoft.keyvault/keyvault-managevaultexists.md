<properties
	pageTitle="Managing an Existing Key Vault"
	description="Managing an Existing Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="jalichwa"
	displayOrder="17"
	selfHelpType="generic"
	supportTopicIds="32375296"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="ef2146e8-0e56-4e59-b7fa-629446d88d7f"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Managing an Existing Key Vault
## **Recommended Steps**

* [Create and manage Key Vault with CLI](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
* [Secure your Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-secure-your-key-vault)<br>

### Troubleshooting

* How can I backup key vault or key vault objects?<br>

	You can backup individual key vault objects ie. Backup Key, Backup Secret, Backup Certificate [Using Azure CLI](https://docs.microsoft.com/rest/api/keyvault/backupkey), [Using Powershell](https://docs.microsoft.com/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey?view=azurermps-6.13.0). The backup command backs up all versions of each secret. If you have a secret with a large number of previous versions (more than 10), the request size might exceed the allowed maximum and the operation might fail.

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>

	[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>

	[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
* [Key Vault key rotation and auditing](https://docs.microsoft.com/azure/key-vault/key-vault-key-rotation-log-monitoring)<br>
* [Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)
