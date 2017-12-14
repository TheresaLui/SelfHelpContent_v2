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
* Next you need to [Register the application in Azure Active Directory](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br> Then, authorize the Application to use secrets and keys.<br>

**Troublshooting**

* To see how to associate a certificate with an Azure AD application look at [Getting Started with Key Vault for Certificates](https://blogs.technet.microsoft.com/kv/2016/09/26/get-started-with-azure-key-vault-certificates/) <br>
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
[Key Vault Throttling limits](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-throttling)<br>