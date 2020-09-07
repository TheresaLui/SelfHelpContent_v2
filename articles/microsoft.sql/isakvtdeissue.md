<properties
	pageTitle="Database Connectivity issue due to inaccessible TDE protector"
	description="IsAKVTDEIssue"
	infoBubbleText="Found issue with TDE configuration. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="aliceku"
    ms.author="aliceku"
	displayOrder=""
	articleId="IsAKVTDEIssue_5F17762E-DC15-4EEF-81BB-C8FBAC9033CA"
	diagnosticScenario=""
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Connection attempts to your database **<!--$DatabaseName--> DatabaseName <!--/$DatabaseName-->** have recently failed, because the server's TDE protector in Azure Key Vault is inaccessible. After a server loses access to the TDE Protector, all connections to the encrypted databases under the server are blocked, and these databases go offline and get dropped within 24 hours. Old backups encrypted with the unavailable key are no longer accessible.
<!--/issueDescription-->

Your server lost access to the TDE protector due to one of the following root causes:

1. The Key Vault or the Key Vault Key might have been deleted from your subscription <br>
2. The permissions required by the Key Vault Key might have been removed or updated
3. Expired Key Vault Key: if a key already used as a TDE Protector for a server was accidentally configured with an expiration date in Azure Key Vault
4. Deleted Server Identity in Azure Active Directory (AAD). A server's access to Key Vault is managed through the server's unique AAD identity. If the server's identity was deleted from AAD, the server has lost access to the Key Vault.<br>

## **Recommended Steps**

1. Using Azure Power Shell login to Azure:

```	
// Login to your azure account
Login-AzureRMAccount -Environment [env]
```

```
// Get the right subscription where the SQL Server and your Key Vault key belongs
Get-AzureRmSubscription -SubscriptionId [SubscriptionId]
```

1. Get the current encryption protector on the Server to see the Azure Key Vault Key protecting the database(s). This will return the Azure Key Vault Uri.
1. Check if the Key Vault Key has the right permissions. The required permissions on the key are wrapKey and unwrapKey.<br>

```
// To get the server information
$server = Get-AzureRmSqlServer -ResourceGroupName [SQLDatabaseResourceGroupName]  -ServerName $server.ResourceGroupName
```

```
//Gets the server key information
$serverKey = Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName $server.ServerName -ResourceGroupName $server.ResourceGroupName
```

```
// Updates the Key Vault Key operation permission
$mykeyOps = @('wrapKey', 'unwrapKey')
set-AzureKeyVaultKeyAttribute  -VaultName [VaultName]  -KeyName [KeyName]  -KeyOps $mykeyOps
```

1. Check if the Azure Active Directory Principal Id for the Server has permissions to the key. The server principal required permissions are get, wrapKey, and unwrapKey. <br>

```
// To grant permission to the principal
Set-AzureRmKeyVaultAccessPolicy -VaultName [KeyVaultName]  -ObjectId  $server.Identity.PrincipalId  -PermissionsToKeys get, wrapKey, unwrapKey
```

For more information, please refer to [Transparent Database Encryption with Bring Your own Key Support](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption-byok-azure-sql).
