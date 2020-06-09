<properties
	pageTitle="Application Cannot Obtain or Use a Key"
	description="Application Cannot Obtain or Use a Key"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="jalichwa"
	displayOrder="16"
	selfHelpType="generic"
	supportTopicIds="32375283"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="c91b46a1-97cf-4619-9767-45d0c3e0fdd8"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Application Cannot Obtain or Use a Key
## **Recommended Steps**

* Authorize an application to use a key or secret. Assume for this example that the service principal name (spn) is "yourSPN" and that the user principal name is "yourUPN": 

```
az keyvault set-policy --name 'ContosoKeyVault' --spn yourSPN --key-permissions decrypt sign
az keyvault set-policy --name 'ContosoKeyVault' --upn yourUPN --secret-permissions get
```

**Troubleshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>

	[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)<br>

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>
	
	[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)<br>

## **Recommended Documents**

* [Use an App Service Managed Identity to Access Key Vault](https://docs.microsoft.com/azure/key-vault/managed-identity)<br>
* [Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
* [Create and Manage using CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
* [Using Managed Storage Account Keys](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-storage-keys)<br>
* [Security Worlds and Geographic Boundaries](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-security-worlds)<br>
* [Using Soft-Delete with Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)<br>
* [Using Soft-Delete with Key Vault with CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-cli)<br>
* [Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
