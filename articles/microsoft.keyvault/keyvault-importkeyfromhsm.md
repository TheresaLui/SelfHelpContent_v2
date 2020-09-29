<properties
	pageTitle="How to Generate and Transfer HSM-protected Keys for Azure Key Vault"
	description="Importing a key from a HSM to Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="jalichwa"
	displayOrder="8"
	selfHelpType="generic"
	supportTopicIds="32375292"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="a326f60c-684b-4df2-8b83-15e5dd4068c0"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Generate and Transfer HSM-protected Keys for Azure Key Vault
## **Recommended Steps**

* How to import [HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)
* Before importing a HSM-protected key to key vault you will need to download the BYOK toolset. Please note that is feature is available on Windows only.
* Transfer your key to your key vault

### **Troubleshooting**

* How to Setup a Key Vault for HSM-protected Keys?

	There are two different types of Key Vaults: "Premium" and "Standard". One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys.<br>

## **Recommended Documents**

* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
* [Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
* [How to Generate and Transfer HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)<br>
