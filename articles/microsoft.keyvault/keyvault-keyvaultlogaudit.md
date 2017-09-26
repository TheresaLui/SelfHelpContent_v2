<properties
	pageTitle="Azure Key Vault Logging and Auditing"
	description="Logging and Auditing with Azure Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds="32375294"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Logging and Auditing with Key Vault 
## **Recommended Steps**

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
[Set up key vault with end-to-end key rotation and auditing](https://docs.microsoft.com/azure/key-vault/key-vault-key-rotation-log-monitoring)
* On an existing key vault you can enable logging with the following set of PowerShell commands. The first command is used to login via PowerShell to your Azure account.<br>
    ``` 
        Login-AzureRmAccount
        $sa = New-AzureRmStorageAccount -ResourceGroupName 'ContosoResourceGroup' -Name '<yourStorageAccountName>' -Type Standard\_LRS -Location 'East US'
        $kv = Get-AzureRmKeyVault -VaultName 'testVault'
        Set-AzureRmDiagnosticSetting -ResourceId $kv.ResourceId -StorageAccountId $sa.Id -Enabled $true -Categories AuditEvent 
	```
**Troublshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>
[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)
* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>
[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[Logging with Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-logging)<br>
[Set up key vault with end-to-end key rotation and auditing](https://docs.microsoft.com/azure/key-vault/key-vault-key-rotation-log-monitoring)<br>