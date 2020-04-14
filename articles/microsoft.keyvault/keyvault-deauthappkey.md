<properties
	pageTitle="Authorizing and Deauthorizing Applications to Use Keys"
	description="Authorizing and Deauthorizing Applications to Use Keys"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="jalichwa"
	displayOrder="13"
	selfHelpType="generic"
	supportTopicIds="32375284"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="a6ae6509-9a17-4c40-94d7-7c7d580ed8db"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Authorizing and Deauthorizing Applications to Use Keys
## **Recommended Steps**

* Authorize an application to use a key or secret. Assume for this example that the service principal name (spn) is "yourSPN" and that the user principal name is "yourUPN":

```
az keyvault set-policy --name 'ContosoKeyVault' --spn yourSPN --key-permissions decrypt sign
az keyvault set-policy --name 'ContosoKeyVault' --upn yourUPN --secret-permissions get
```

* Deauthorizing application to use keys: `az keyvault delete-policy --name 'ContosoKeyVault' --upn yourUPN`

**Troubleshooting**

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?

	[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)<br>

## **Recommended Documents**

* [Use an App Service Managed Identity to Access Key Vault](https://docs.microsoft.com/azure/key-vault/managed-identity)<br>
* [Azure CLI 2.0 Documentation](https://docs.microsoft.com/cli/azure/keyvault?view=azure-cli-latest#az_keyvault_delete_policy)<br>
* [Using Soft-Delete with Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)<br>
* [Using Soft-Delete with Key Vault with CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-cli)<br>
* [Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
* [Using Managed Storage Account Keys](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-storage-keys)<br>
* [Security Worlds and Geographic Boundaries](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-security-worlds)
