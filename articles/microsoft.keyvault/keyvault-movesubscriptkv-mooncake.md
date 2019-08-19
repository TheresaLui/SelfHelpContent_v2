<properties
	pageTitle="Moving a Vault to Another Subscription"
	description="Moving a Vault From One Subscription to Another"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="fhokholdMSFT"
	displayOrder="16"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="optional"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="keyvault-movesubscriptkv-mooncake"
/>

# How to Change Key Vault Type for Azure Key Vault

## **Recommended steps**

* There are two different types of Key Vaults: "Premium" and "Standard". Here is an example of how to create a "Premium" and "Standard" key vault, respectively. One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys. Assume that your vault name is "myvault" and your resource group name is "yourResourceGroup".

**Troubleshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?

    [Change a key vault tenant ID after a subscription move](https://docs.azure.cn/key-vault/key-vault-subscription-move-fix)

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?

    [Grant permission to many applications to access a key vault](https://docs.azure.cn/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-get-started)
* [Create and Manage using CLI 2.0](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)