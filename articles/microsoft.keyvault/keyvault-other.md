<properties
	pageTitle="Other Scenarios for Key Vault"
	description="Other Scenarios for Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32382911"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# Other Scenarios for Key Vault related tasks
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

**Sample usage of Managed Storage Account Keys**

* We assume that our storage resource is located at the following. 
Storage resource: /subscriptions/subscriptionId/resourceGroups/yourresgroup1/providers/Microsoft.Storage/storageAccounts/yourtest1
Also, let's assume that the name of our key vault is: yourtest1<br>
    ```
        Get-AzureRmADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
    ```
* The output will include your ServicePrincipal, which we will call yourServicePrincipalId. You can find your user principal Id using.<br>
    ```
        Get-AzureRmADUser -SearchString "your name" 
    ```
* Please make sure you have permissions to storage set to all using the user principal Id which we will call yourUserPrincipalId.<br> 
    ```
        Set-AzureRmKeyVaultAccessPolicy -VaultName 'yourtest1' -ObjectId yourUserPrincipalId -PermissionsToStorage all
    ```
* Firstly, we need to give the Key Vault service access to the storage accounts, before we can create a managed storage account and SAS definitions.<br>
    ```
        New-AzureRmRoleAssignment -ObjectId yourServicePrincipalId -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope '/subscriptions/subscriptionId/resourceGroups/yourresgroup1/providers/Microsoft.Storage/storageAccounts/yourtest1'
    ```
* Now let's create a Managed Storage Account and two SAS definitions (the account SAS provides access to the blob service with different permissions).<br>
    ```
        Add-AzureKeyVaultManagedStorageAccount -VaultName yourtest1 -Name msak01 -AccountResourceId /subscriptions/subscriptionId/resourceGroups/yourresgroup1/providers/Microsoft.Storage/storageAccounts/yourtest1 -ActiveKeyName key2 -DisableAutoRegenerateKey
    ```
* Side note: If you would like to set the regeneration period it can be done using the following commands for example.<br>
    ```
        $regenPeriod = [System.Timespan]::FromDays(3)
        Add-AzureKeyVaultManagedStorageAccount -VaultName yourtest1 -Name msak01 -AccountResourceId /subscriptions/subscriptionId/resourceGroups/yourresgroup1/providers/Microsoft.Storage/storageAccounts/yourtest1 -ActiveKeyName key2 -RegenerationPeriod $regenPeriod
    ```
* Now let's set the SAS definitions in Key Vault for the now managed storage account.<br>
    ```
        Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob -ResourceType Container,Service -VaultName yourtest1  -AccountName msak01 -Name blobsas1 -Protocol HttpsOnly -ValidityPeriod ([System.Timespan]::FromDays(1)) -Permission Read,List
        Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob -ResourceType Container,Service,Object -VaultName yourtest1  -AccountName msak01 -Name blobsas2 -Protocol HttpsOnly -ValidityPeriod ([System.Timespan]::FromDays(1)) -Permission Read,List,Write
    ```
* Next lets get the corresponding SAS tokens and make calls to storage.<br>
    ```
        $sasToken1 = (Get-AzureKeyVaultSecret -VaultName yourtest1 -SecretName msak01-blobsas1).SecretValueText
        $sasToken2 = (Get-AzureKeyVaultSecret -VaultName yourtest1 -SecretName msak01-blobsas2).SecretValueText
    ```
* We notice that trying to access with $sastoken1 fails, but that we are able to access with $sastoken2.<br>
    ```
        $context1 = New-AzureStorageContext -SasToken $sasToken1 -StorageAccountName yourtest1
        $context2 = New-AzureStorageContext -SasToken $sasToken2 -StorageAccountName yourtest1
        Set-AzureStorageBlobContent -Container containertest1 -File "abc.txt"  -Context $context1
        Set-AzureStorageBlobContent -Container cont1-file "file.txt"  -Context $context2
    ```
* So we are able access the storage blob content with the SAS token that has write access.<br>
* Cmdlets relevant to the feature are:<br>
    ```
        Get-AzureKeyVaultManagedStorageAccount
        Add-AzureKeyVaultManagedStorageAccount
        Get-AzureKeyVaultManagedStorageSasDefinition
        Update-AzureKeyVaultManagedStorageAccountKey
        Remove-AzureKeyVaultManagedStorageAccount
        Remove-AzureKeyVaultManagedStorageSasDefinition
        Set-AzureKeyVaultManagedStorageSasDefinition
    ```    
**Troublshooting**

* How do I associate a certificate with an Azure AD application?<br>
	```
		$x509 = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
		$x509.Import("C:\data\KVWebApp.cer")
		$credValue = [System.Convert]::ToBase64String($x509.GetRawCertData())

		# If you used different dates for makecert then adjust these values
		$now = [System.DateTime]::Now
		$yearfromnow = $now.AddYears(1)

		$adapp = New-AzureRmADApplication -DisplayName "KVWebApp" -HomePage "http://kvwebapp" -IdentifierUris "http://kvwebapp" -CertValue $credValue -StartDate $now -EndDate $yearfromnow

		$sp = New-AzureRmADServicePrincipal -ApplicationId $adapp.ApplicationId

		Set-AzureRmKeyVaultAccessPolicy -VaultName 'contosokv' -ServicePrincipalName $sp.ServicePrincipalName -PermissionsToSecrets all -ResourceGroupName 'contosorg'

		# get the thumbprint to use in your app settings
		$x509.Thumbprint
	```
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
[Code Samples for Key Vault](https://azure.microsoft.com/resources/samples/?service=key-vault&sort=0)<br>