<properties
	pageTitle="How to Use Key Vault with an Application"
	description="Using key vault with an Application"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="jalichwa"
	displayOrder="7"
	selfHelpType="generic"
	supportTopicIds="32375291"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="a3f8dd78-7c00-441f-93af-e85d80937976"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Develop an Application to Use Key Vault
## **Recommended Steps**

* [Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)
* [Use an App Service Managed Identity to Access Key Vault](https://docs.microsoft.com/azure/key-vault/managed-identity)

**Troubleshooting**

* To see how to associate a certificate with an Azure AD application look at [Getting Started with Key Vault for Certificates](https://blogs.technet.microsoft.com/kv/2016/09/26/get-started-with-azure-key-vault-certificates/)<br>
* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>

	[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>
	
	[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
* [Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
* [Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-use-from-web-application)<br>
* [Key Vault Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)<br>
* [Azure Code Samples](https://azure.microsoft.com/resources/samples/?service=key-vault&sort=0)<br>
* [Certificate Based Authentication with Java](https://github.com/Azure-Samples/key-vault-java-certificate-authentication)<br>
