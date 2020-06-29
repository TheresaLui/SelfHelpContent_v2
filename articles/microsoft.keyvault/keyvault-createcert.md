<properties
	pageTitle="How to Create Certificate in Key vault"
	description="How to Create or export Certificate in Key vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="sebansal"
	ms.author="sebansal"
	displayOrder="19"
	selfHelpType="generic"
	supportTopicIds="32739895"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-createcert"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Create Certificate
## **Recommended Steps**

* [Certificate creation methods](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate)
* [Creating Self-Signed Certificate](https://docs.microsoft.com/azure/key-vault/certificates/quick-create-portal)
* [Creating and merging certificate signing request (CSR)](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-signing-request)
* [Creating certificate with CA not partnered with Key vault](https://docs.microsoft.com/azure/key-vault/certificates/certificate-scenarios#creating-a-certificate-with-a-ca-not-partnered-with-key-vault)
* [Monitor and manage certificate creation](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-scenarios)


### **Troubleshooting**

* I had created a certificate and it is near expiry. What happens if it expires?
	
	If a Key Vault certificate expires, it's addressable key and secret become inoperable. [Configure Certificate's Life cycle attributes](https://docs.microsoft.com/azure/key-vault/certificates/tutorial-rotate-certificates).

* How to export a certificate from Key vault?
	
	You can download the certificate in .cer, .pfx or .pem format. [Exporting certificate from Azure portal](https://docs.microsoft.com/azure/key-vault/certificates/quick-create-portal#export-certificate-from-key-vault).

* Error type : Access denied or user is unauthorized to create certificate 
	
	Access control for certificates is managed by Key Vault, and is provided by the Key Vault that contains those certificates. This operation requires the certificates/create permission. [Read more](https://docs.microsoft.com/azure/key-vault/certificates/about-certificates#certificate-access-control)

* Error type : Conflict when creating a certificate
	
	Certificate name should be unique. Certificate with the same name might be in soft-deleted state, [view deleted certificate](https://docs.microsoft.com/rest/api/keyvault/getdeletedcertificate/getdeletedcertificate)

## **Recommended Documents**

* [Creating Certificate using CLI](https://docs.microsoft.com/rest/api/keyvault/createcertificate/createcertificate)
* [Setting Certificate Issuer using CLI](https://docs.microsoft.com/rest/api/keyvault/setcertificateissuer/setcertificateissuer)
* [About Azure Key Vault certificates](https://docs.microsoft.com/azure/key-vault/certificates/about-certificates)
