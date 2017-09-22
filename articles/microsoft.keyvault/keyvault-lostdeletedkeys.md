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

##Troublshooting

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>
[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)
* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>
[Grant permission to many applications to access a key vault](https://docs.microsoft.com/en-us/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**
[Using Soft-Delete with Key Vault with PowerShell](https://docs.microsoft.com/en-us/azure/key-vault/key-vault-soft-delete-powershell)<br>
[Using Soft-Delete with Key Vault with CLI 2.0](https://docs.microsoft.com/en-us/azure/key-vault/key-vault-soft-delete-cli)<br>
[Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
[Understanding Backup and Restore Behavior in Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-security-worlds)<br>