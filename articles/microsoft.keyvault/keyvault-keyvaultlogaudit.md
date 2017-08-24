<properties
	pageTitle="Azure Key Vault Logging and Auditing"
	description="Logging and Auditing with Azure Key Vault"
	service="Microsoft.keyvault"
	resource="keyvault"
	authors="fhokholdMSFT"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32375294"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Logging and Auditing with Key Vault 
## **Recommended steps**

* Logging with Azure Key Vault<br>
[Using Logging with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-logging)
* Before using logging you will need to have a key vault set up. This is how to create a key vault with a key and secret in it using Azure CLI 2.0.<br>
	```
        az login 
        az group create --name "ContosoResourceGroup" --location "East Asia" 
        az provider register --namespace Microsoft.KeyVault 
        az keyvault create --name "testVault" --resource-group "ContosoResourceGroup" --location "East Asia" --enable-soft-delete 
        az keyvault key create --vault-name 'testVault' --name 'ContosoFirstKey' --protection software 
        az keyvault secret set --vault-name 'testVault' --name 'SQLPassword' --value 'Pa$$w0rd' 
	``` 
* Auditing with Key Vault<br>
[Set up Key Vault with end-to-end key rotation and auditing](https://docs.microsoft.com/azure/key-vault/key-vault-key-rotation-log-monitoring)
## **Recommended documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[Logging with Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-logging)<br>
[Set up Key Vault with end-to-end key rotation and auditing](https://docs.microsoft.com/azure/key-vault/key-vault-key-rotation-log-monitoring)

