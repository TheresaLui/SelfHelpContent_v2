<properties
	pageTitle="Lost or Deleted Keys and Secrets in Key Vault"
	description="Using Soft-Delete and Backup and Restore Behavior with Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32375295"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# Lost or Deleted Keys and Secrets in Key Vault
## **Recommended steps**

* Using Soft-Delete with Key Vault<br>
[Using Soft-Delete and Backup and Restore Behavior with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)
* Before using soft delete you will need to have a key vault set up. This is how to create a key vault with a key and secret in it using Azure CLI 2.0.<br>  
    ```
        az login 
        az group create --name "ContosoResourceGroup" --location "East Asia" 
        az provider register --namespace Microsoft.KeyVault 
        az keyvault create --name "testVault" --resource-group "ContosoResourceGroup" --location "East Asia" --enable-soft-delete 
        az keyvault key create --vault-name 'testVault' --name 'ContosoFirstKey' --protection software 
        az keyvault secret set --vault-name 'testVault' --name 'SQLPassword' --value 'Pa$$w0rd' 
    ```
* The following are commands for Azure CLI 2.0 with Soft-Delete.<br>
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

## **Recommended Documents**
[Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
[Understanding Backup and Restore Behavior in Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-security-worlds)<br>