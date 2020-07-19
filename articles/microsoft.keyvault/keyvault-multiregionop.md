<properties
	pageTitle="Configuring an Application for Multi-Region Redundant Operation"
	description="Configuring an Application for Multi-Region Redundant Operation"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="jalichwa"
	displayOrder="21"
	selfHelpType="generic"
	supportTopicIds="32375287"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="cb727e8d-89ea-4d5e-ba1f-d1679f0ecb35"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to configure an application for multi-region redundant operation
## **Recommended steps**

* Key Vault features [multiple layers of redundancy in order to maintain availability](https://docs.microsoft.com/azure/key-vault/key-vault-disaster-recovery-guidance)<br>

**Troubleshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>
	
	[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>

	[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Availability and Redundancy Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-disaster-recovery-guidance)<br>
* [Azure Key Vault Security Worlds](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-security-worlds)<br>
* [Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
* [How to Generate and Transfer HSM-protected Keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)<br>
* [Create and Manage using CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
