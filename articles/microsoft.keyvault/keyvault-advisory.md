<properties
	pageTitle="Advisory for Key Vault"
	description="Advisory for Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="10"
	selfHelpType="resource"
	supportTopicIds="32452742"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# Advisory for Key Vault related tasks
## **Recommended steps**

* How to Create and Manage a Key Vault<br>
[Key Vault Getting Started Guide in PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)
* The following commands are for setting up a key vault with a key and secret in it using Azure CLI 2.0. Premium SKU<br>  
    ```
        az login 
        az group create --name "ContosoResourceGroup" --location "East Asia" 
        az provider register --namespace Microsoft.KeyVault 
        az keyvault create --name "testVault" --resource-group "ContosoResourceGroup" --location "East Asia" --enable-soft-delete 
        az keyvault key create --vault-name 'testVault' --name 'ContosoFirstKey' --protection software 
        az keyvault secret set --vault-name 'testVault' --name 'SQLPassword' --value 'Pa$$w0rd' 
    ```

* Next you need to [Register the application in Azure Active Directory](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br> Then, authorize the Application to use secrets and keys.<br>
    ``` 
		az keyvault set-policy --name 'testVault' --spn yourApplicationClientId --key-permissions decrypt sign 
    	az keyvault set-policy --name 'testVault' --spn yourApplicationClientId --secret-permissions get 
	```
* The following are commands for Azure CLI 2.0 with Soft-Delete. Examples for Soft-Delete with PowerShell are in a link below.<br>
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
* On an existing key vault you can enable logging with the following set of PowerShell commands. The first command is used to login via PowerShell to your Azure account.<br>
    ``` 
        Login-AzureRmAccount
        $sa = New-AzureRmStorageAccount -ResourceGroupName 'ContosoResourceGroup' -Name '<yourStorageAccountName>' -Type Standard\_LRS -Location 'East US'
        $kv = Get-AzureRmKeyVault -VaultName 'testVault'
        Set-AzureRmDiagnosticSetting -ResourceId $kv.ResourceId -StorageAccountId $sa.Id -Enabled $true -Categories AuditEvent 
	```
    
##Troublshooting

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>
[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)
* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>
[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-use-from-web-application)<br>
[Using Soft-Delete with Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)<br>
[Using Soft-Delete with Key Vault with CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-cli)<br>
[Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
[Azure Code Samples](https://azure.microsoft.com/resources/samples/?service=key-vault&sort=0)<br>
[Key Vault Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)<br>
[How to Generate and Transfer HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)<br>
[Getting Started with Certificates in Key Vault](https://blogs.technet.microsoft.com/kv/2016/09/26/get-started-with-azure-key-vault-certificates/)<br>
[Logging with Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-logging)<br>
[Set up key vault with end-to-end key rotation and auditing](https://docs.microsoft.com/azure/key-vault/key-vault-key-rotation-log-monitoring)<br>
[Key Vault Storage Account Keys](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-storage-keys)<br>
[Understanding Backup and Restore Behavior in Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-security-worlds)<br>
[Secure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-secure-your-key-vault)<br>