<properties
	pageTitle="Moving a Vault to Another Subscription"
	description="Moving a Vault From One Subscription to Another"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="12"
	selfHelpType="resource"
	supportTopicIds="32375297"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Change Key Vault Type for Azure Key Vault
## **Recommended steps**

* There are two different types of Key Vaults: "Premium" and "Standard". Here is an example of how to create a "Premium" and "Standard" key vault, respectively. One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys. Assume that your vault name is "myvault" and your resource group name is "yourResourceGroup".<br>

**Troublshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>
[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)
* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>
[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[How to Generate and Transfer HSM-protected Keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)<br>
[Create and Manage using CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>