<properties
	pageTitle="How to Generate and Transfer HSM-protected Keys for Azure Key Vault"
	description="Importing a key from a HSM to Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="10"
	selfHelpType="resource"
	supportTopicIds="32375292"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="MoonCake"
	articleId="a326f60c-684b-4df2-8b83-15e5dd4068c0"
/>

# How to Generate and Transfer HSM-protected Keys for Azure Key Vault

## **Recommended Steps**

* Before importing a HSM-protected key to key vault you will need to download the BYOK toolset. Please note that is feature is available on Windows only
* The link aobve shows you how to generate a key using Thales generatekey program and transfer your key to your key vault.

**Troublshooting**

* How to Setup a Key Vault for HSM-protected Keys?
* There are two different types of Key Vaults: "Premium" and "Standard". One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys.

## **Recommended Documents**

* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)
* [Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-get-started)