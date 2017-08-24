<properties
	pageTitle="Managing Users and Keys in Key Vault"
	description="Managing Users and Keys in Key Vault"
	service="vaults"
	resource="keyvault"
	authors="fhokholdMSFT"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32375281"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# Managing Users and Keys in Key Vault
## **Recommended steps**

* Managing Users and Keys<br>
[Using Managed Storage Account Keys](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-storage-keys)
[Using Soft-Delete and Backup and Restore Behavior with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)
* Before using soft delete or managed storage account keys you will need to have a key vault set up. This is how to create a key vault with a key and secret in it using Azure CLI 2.0.<br>
    ```
        az login 
        az group create --name "ContosoResourceGroup" --location "East Asia" 
        az provider register --namespace Microsoft.KeyVault 
        az keyvault create --name "testVault" --resource-group "ContosoResourceGroup" --location "East Asia" --enable-soft-delete 
        az keyvault key create --vault-name 'testVault' --name 'ContosoFirstKey' --protection software 
        az keyvault secret set --vault-name 'testVault' --name 'SQLPassword' --value 'Pa$$w0rd' 
    ```
* The following are commands for Azure CLI 2.0 with Soft-Delete.
    ``` 
        Delete key:
        az keyvault key delete --name ContosoFirstKey --vault-name testVault  
        List deleted keys:
        az keyvault key list-deleted --vault-name testVault  
        Recover Key:
        az keyvault key recover --name ContosoFirstKey --vault-name testVault  
        Permanently Delete Key:
        az keyvault key purge --name ContosoFirstKey --vault-name testVault 
    ```
## **Recommended documents**
[Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
[Create and Manage using CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Security Worlds and Geographic Boundaries](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-security-worlds)
