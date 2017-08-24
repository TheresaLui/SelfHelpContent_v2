<properties
	pageTitle="How to Create and Manage a Key Vault"
	description="Creating a New Key Vault"
	service="vaults"
	resource="keyvault"
	authors="fhokholdMSFT"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32375289"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Create and Manage a Key Vault
## **Recommended steps**

* Create a New Key Vault<br>
[Key Vault Getting Started Guide](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)
* This is how to create a key vault using Azure CLI 2.0.<br>
    ``` 
		az login 
		az group create --name "ContosoResourceGroup" --location "East Asia" 
		az provider register --namespace Microsoft.KeyVault 
		az keyvault create --name "testVault" --resource-group "ContosoResourceGroup" --location "East Asia" --enable-soft-delete 
	```
* You can also create a Key Vault using the Azure Portal.<br>
[Create a Key Vault with Azure Portal](https://ms.portal.azure.com/#create/Microsoft.KeyVault)
## **Recommended documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)


