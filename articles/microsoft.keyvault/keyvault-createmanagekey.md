<properties
	pageTitle="How to Create and Manage Keys"
	description="How to Create and Manage Keys"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="19"
	selfHelpType="resource"
	supportTopicIds="32375290"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Create and Manage Keys
## **Recommended steps**

* Create a new key vault and a key inside the vault.<br>
[Key Vault Getting Started Guide](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)
* You can also create a key vault using the Azure Portal.<br>
[Create a Key Vault with Azure Portal](https://ms.portal.azure.com/#create/Microsoft.KeyVault)

**Troublshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>
[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)
* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>
[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)