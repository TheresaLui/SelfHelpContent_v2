<properties
	pageTitle="Advisory for Key Vault"
	description="Advisory for Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="jalichwa"
	displayOrder="10"
	selfHelpType="generic"
	supportTopicIds="32452742"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="ee2740e9-e40c-4c32-ab2c-0ec8414b28c3"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Advisory for Key Vault related tasks
## **Recommended Steps**

* [Key Vault Get Started](https://docs.microsoft.com/azure/key-vault/key-vault-overview)
* [About Key Vault](https://docs.microsoft.com/azure/key-vault/basic-concepts)
* [Key Vault Best Practices](https://docs.microsoft.com/azure/key-vault/key-vault-best-practices)

**Troubleshooting**

* To see how to associate a certificate with an Azure AD application look at [Getting Started with Key Vault for Certificates](https://blogs.technet.microsoft.com/kv/2016/09/26/get-started-with-azure-key-vault-certificates/)

* How can I **monitor how and when your key vaults are accessed**, and by whom? <br>
You can turn on [logs on Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-logging) and to monitor health of key vault [configure metrics and alerting for Key Vault](https://docs.microsoft.com/azure/key-vault/general/alert)

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>
	
	[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)

* I have several (over 1024) applications that need to access a key vault. Since Key Vault only allows 1024 access control entries, how can I achieve that?<br>
	
	[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
* [Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
* [Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-use-from-web-application)<br>
* [Using Soft-Delete with Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)<br>
* [Using Soft-Delete with Key Vault with CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-cli)<br>
* [Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
* [Azure Code Samples](https://azure.microsoft.com/resources/samples/?service=key-vault&sort=0)<br>
* [Key Vault Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)<br>
* [How to Generate and Transfer HSM-protected Keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)<br>
* [Getting Started with Certificates in Key Vault](https://blogs.technet.microsoft.com/kv/2016/09/26/get-started-with-azure-key-vault-certificates/)<br>
* [Logging with Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-logging)<br>
* [Set Up Key Vault with End-to-End Key Rotation and Auditing](https://docs.microsoft.com/azure/key-vault/key-vault-key-rotation-log-monitoring)<br>
* [Key Vault Storage Account Keys](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-storage-keys)<br>
* [Understanding Backup and Restore Behavior in Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-security-worlds)<br>
* [Secure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-secure-your-key-vault)<br>
* [Key Vault Throttling Limits](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-throttling)<br>
