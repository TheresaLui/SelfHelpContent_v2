<properties
	pageTitle="Importing Existing Keys Into Key Vault"
	description="Importing Existing Keys Into Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="sudbalas"
	displayOrder="20"
	selfHelpType="generic"
	supportTopicIds="32375293"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="917e26d0-971a-44b3-9c12-da53dacc5c4c"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Import Existing Keys into a Key Vault
## **Recommended Steps**

* If you are moving your key vault to a new subscription, please see the following document. [Azure Key Vault Subscription Move](https://docs.microsoft.com/azure/key-vault/general/keyvault-move-subscription)
* [Add/Import Secrets to Key Vault using CLI](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2#adding-a-key-secret-or-certificate-to-the-key-vault)<br>
* [CLI Developer Guide for Importing Keys](https://docs.microsoft.com/cli/azure/keyvault/key?view=azure-cli-latest#az-keyvault-key-import) <br>

### **Troubleshooting**

* How do I Set up a Key Vault for HSM-protected Keys?

	There are two different types of Key Vaults: "Premium" and "Standard". One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys.<br>

## **Recommended Documents**

* [Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/quick-create-powershell)<br>
* [How to Generate and Transfer HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)<br>
