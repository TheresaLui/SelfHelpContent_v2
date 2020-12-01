<properties
	pageTitle="How to Import Certificate in Key vault"
	description="How to Import/Upload Certificate in Key vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="sebansal"
	ms.author="sebansal"
	displayOrder="19"
	selfHelpType="generic"
	supportTopicIds="32739896"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-importcert"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Import Certificate
## **Recommended Steps**

* [Answered questions about issues related to importing certificate in key vault](https://docs.microsoft.com/azure/key-vault/certificates/import-cert-faqs)
* [How to import certificate in Key vault](https://docs.microsoft.com/azure/key-vault/certificates/tutorial-import-certificate)
* [How to export certificate from Key vault](https://docs.microsoft.com/azure/key-vault/certificates/how-to-export-certificate)
* [How to create and merge certificate signing request (CSR)](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-signing-request)


### **Troubleshooting**

* What are the supported certificate formats for importing in Key vault?
	
	In Azure Key Vault, supported certificate formats are PFX and PEM. [Read more](https://docs.microsoft.com/azure/key-vault/certificates/tutorial-import-certificate#import-a-certificate-to-key-vault)

* Error when importing certificate via Portal "Something went wrong". How to investigate further?
 	
	Make sure the import file is in [correct format](https://docs.microsoft.com/azure/key-vault/certificates/certificate-scenarios#formats-of-import-we-support). It is required for certificate (pem or pfx) to have a private key for import. To see more descriptive error, import the certificate file via [Azure CLI](https://docs.microsoft.com/cli/azure/keyvault/certificate?view=azure-cli-latest#az-keyvault-certificate-import) or [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate?view=azurermps-6.13.0).

* For Error type: Access denied or user is unauthorized to import certificate
	
   Access control for certificates is managed by Key Vault, and is provided by the Key Vault that contains those certificates. This operation requires the certificates/import permission. Navigate to where the Key Vault is located, you will need to grant the user appropriate permissions under **access policies**. Navigate to the **KeyVault> Access policies > Add Access Policy > Select Certificate Permissions (or as you want the permissions) > Principal > search for and then add user's email**. [Read more](https://docs.microsoft.com/azure/key-vault/certificates/about-certificates#certificate-access-control)

* Importing expired certificate in Azure Key vault
	
	As per design the expired PFX certificates won't be able to be imported to Azure Key Vault.

* After importing protected certificate into keyvault and then downloading it from key vault, I am not able to see the password associated with the certificate?
 	
	The uploaded protected certificate after storage into keyvault would not save password associated with it. It is only required once during the import operation.

## **Recommended Documents**

* [Importing Certificate using CLI](https://docs.microsoft.com/rest/api/keyvault/importcertificate/importcertificate)
* [Setting Certificate Issuer using CLI](https://docs.microsoft.com/rest/api/keyvault/setcertificateissuer/setcertificateissuer)
* [About Azure Key Vault certificates](https://docs.microsoft.com/azure/key-vault/certificates/about-certificates)
