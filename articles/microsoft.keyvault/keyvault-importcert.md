<properties
	pageTitle="How to Import Certificate in Key vault"
	description="How to Import Certificate in Key vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="sebansal"
	ms.author="sebansal"
	displayOrder="19"
	selfHelpType="generic"
	supportTopicIds="32739896"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake"
	articleId="keyvault-importcert"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Import Certificate
## **Recommended Steps**

* [Import certificate in Key vault](https://docs.microsoft.com/azure/key-vault/certificates/tutorial-import-certificate)
* [Monitor and manage certificate creation](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-scenarios)



### **Troubleshooting**

* What are the supported certificate formats for importing in Key vault?
	
	In Azure Key Vault, supported certificate formats are PFX and PEM. [Read more](https://docs.microsoft.com/azure/key-vault/certificates/tutorial-import-certificate#import-a-certificate-to-key-vault)

* After importing protected certificate into keyvault and then downloading it from key vault, I am not able to see the password associated with the certificate?
 	
	The uploaded protected certificate after storage into keyvault would not save password associated with it. It is only required once during the import operation.

## **Recommended Documents**

* [Importing Certificate using CLI](https://docs.microsoft.com/rest/api/keyvault/importcertificate/importcertificate)
* [Setting Certificate Issuer using CLI](https://docs.microsoft.com/rest/api/keyvault/setcertificateissuer/setcertificateissuer)
* [About Azure Key Vault certificates](https://docs.microsoft.com/azure/key-vault/certificates/about-certificates)
