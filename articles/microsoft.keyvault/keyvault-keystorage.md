<properties
	pageTitle="Storage Keys with Key Vault"
	description="Storage Keys with Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="11"
	selfHelpType="resource"
	supportTopicIds="32375280"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Use Managed Storage Account Keys with Key Vault
## **Recommended steps**

* Create a New Key Vault<br>
[Key Vault Getting Started Guide](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
* Please make sure you have installed [PowerShell version 4.1.0](https://www.powershellgallery.com/packages/AzureRM/4.1.0). Here are the steps to installing the latest PowerShell from the PowerShell Gallery.There are a few things to check out before using the cmdlets, like ensuring that the Key Vault service is given permissions to the storage keys. There are several supporting links below the following example.<br>

## **Sample usage of Managed Storage Account Keys**
* We assume that our storage resource is located at the following. 
Storage resource: /subscriptions/subscriptionId/resourceGroups/yourresgroup1/providers/Microsoft.Storage/storageAccounts/yourtest1
Also, let's assume that the name of our key vault is: yourtest1
    ```
        Get-AzureRmADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
    ```
* The output will include your  ServicePrincipal, which we will call yourServicePrincipalId. Please make sure you have permissions to storage set to all.
    ```
        Set-AzureRmKeyVaultAccessPolicy -VaultName 'yourtest1' -ObjectId yourServicePrincipalId -PermissionsToStorage all
    ```
* Firstly, we need to give the Key Vault service access to the storage accounts, before we can create a managed storage account and SAS definitions.
    ```
        New-AzureRmRoleAssignment -ObjectId yourServicePrincipalId -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope '/subscriptions/subscriptionId/resourceGroups/yourresgroup1/providers/Microsoft.Storage/storageAccounts/yourtest1'
    ```
* Now let's create a Managed Storage Account and two SAS definitions (the account SAS provides access to the blob service with different permissions).
    ```
        Add-AzureKeyVaultManagedStorageAccount -VaultName yourtest1 -Name msak01 -AccountResourceId /subscriptions/subscriptionId/resourceGroups/yourresgroup1/providers/Microsoft.Storage/storageAccounts/yourtest1 -ActiveKeyName key2 -DisableAutoRegenerateKey
    ```
* Side note: If you would like to set the regeneration period it can be done using the following commands for example.
    ```
        $regenPeriod = [System.Timespan]::FromDays(3)
        Add-AzureKeyVaultManagedStorageAccount -VaultName yourtest1 -Name msak01 -AccountResourceId /subscriptions/subscriptionId/resourceGroups/yourresgroup1/providers/Microsoft.Storage/storageAccounts/yourtest1 -ActiveKeyName key2 -RegenerationPeriod $regenPeriod
    ```
* Now let's set the SAS definitions in Key Vault for the now managed storage account.
    ```
        Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob -ResourceType Container,Service -VaultName yourtest1  -AccountName msak01 -Name blobsas1 -Protocol HttpsOnly -ValidityPeriod ([System.Timespan]::FromDays(1)) -Permission Read,List
        Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob -ResourceType Container,Service,Object -VaultName yourtest1  -AccountName msak01 -Name blobsas2 -Protocol HttpsOnly -ValidityPeriod ([System.Timespan]::FromDays(1)) -Permission Read,List,Write
    ```
* Next lets get the corresponding SAS tokens and make calls to storage.
    ```
        $sasToken1 = (Get-AzureKeyVaultSecret -VaultName yourtest1 -SecretName msak01-blobsas1).SecretValueText
        $sasToken2 = (Get-AzureKeyVaultSecret -VaultName yourtest1 -SecretName msak01-blobsas2).SecretValueText
    ```
* We notice that trying to access with $sastoken1 fails, but that we are able to access with $sastoken2.
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

## **Recommended Documents**
[Key Vault Storage Account Keys with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-storage-keys)<br>
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[Using Soft-Delete with Key Vault with PowerShell](https://docs.microsoft.com/en-us/azure/key-vault/key-vault-soft-delete-powershell)<br>
[Using Soft-Delete with Key Vault with CLI 2.0](https://docs.microsoft.com/en-us/azure/key-vault/key-vault-soft-delete-cli)<br>
[Set up key vault with end-to-end key rotation and auditing](https://docs.microsoft.com/azure/key-vault/key-vault-key-rotation-log-monitoring)<br>