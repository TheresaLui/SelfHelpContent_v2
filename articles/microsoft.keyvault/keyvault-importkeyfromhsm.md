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
* Before importing a HSM-protected key to key vault you will need to have a key vault set up. This is how to create a key vault with a key and secret in it using Azure CLI 2.0.<br>
	```
        az login 
        az group create --name "ContosoResourceGroup" --location "East Asia" 
        az provider register --namespace Microsoft.KeyVault 
        az keyvault create --name "testVault" --resource-group "ContosoResourceGroup" --location "East Asia" --enable-soft-delete 
        az keyvault key create --vault-name 'testVault' --name 'ContosoFirstKey' --protection software 
        az keyvault secret set --vault-name 'testVault' --name 'SQLPassword' --value 'Pa$$w0rd' 
	``` 
	
## **Recommended Documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[How to Generate and Transfer HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)