<properties
	pageTitle="How to Set Key Vault Type for Azure Key Vault"
	description="Set Key Vault Type for Azure Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="jalichwa"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32375286"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="63f236da-16f3-43cf-9918-6b1dfed5086a"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Set Key Vault Type for Azure Key Vault

## **Recommended Steps**

There are two different types of Key Vaults: "Premium" and "Standard". One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys.<br>

Setting Key Vault Type can be done only during creation of key vault.<br>

* When Key Vault is created through Portal, select Standard or Premium pricing tier <br>
* When Key Vault is created through CLI command, use `--SKU parameter` to create standard or premium type. For more information how to create key vault check [Create Key Vault using CLI](https://docs.microsoft.com/cli/azure/keyvault?view=azure-cli-latest#az-keyvault-create).

### **Troubleshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>

	[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>

	[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Creating and Managing Key Vault with Portal](https://docs.microsoft.com/azure/key-vault/quick-create-portal)<br>
* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
* [Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
* [How to Generate and Transfer HSM-protected Keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)<br>
* [Azure CLI Developer Guide](https://docs.microsoft.com/cli/azure/keyvault?view=azure-cli-latest)
