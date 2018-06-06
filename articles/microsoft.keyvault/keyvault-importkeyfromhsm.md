<properties
	pageTitle="How to Generate and Transfer HSM-protected Keys for Azure Key Vault"
	description="Importing a key from a HSM to Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32375292"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Generate and Transfer HSM-protected Keys for Azure Key Vault
## **Recommended Steps**

* How to import a key from a HSM<br>
[HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)
* Before importing a HSM-protected key to key vault you will need to download the BYOK toolset. Please note that is feature is available on Windows only<br>
* The link aobve shows you how to generate a key using Thales generatekey program and transfer your key to your key vault.<br>

**Troublshooting**

* How to Setup a Key Vault for HSM-protected Keys?<br>
* There are two different types of Key Vaults: "Premium" and "Standard". One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys.<br>

## **Recommended Documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[How to Generate and Transfer HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)<br>