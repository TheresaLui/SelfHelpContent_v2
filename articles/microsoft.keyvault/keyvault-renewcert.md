<properties
	pageTitle="Certificate Renewal in Key vault"
	description="Certificate Renewal in Key vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="sebansal"
	ms.author="sebansal"
	displayOrder="19"
	selfHelpType="generic"
	supportTopicIds="32742807"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-renewcert"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Certificate Renewal in Key vault
## **Recommended Steps**

* [Monitor and manage certificate creation](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-scenarios)


### **Troubleshooting**

* I had created a certificate and it is near expiry. What happens if it expires?
	
	If a Key Vault certificate expires, it's addressable key and secret become inoperable. [Configure Certificate's Life cycle attributes](https://docs.microsoft.com/azure/key-vault/certificates/tutorial-rotate-certificates).

* How do I autorotate certificate stored in key vault?
	
	Azure Key vault automatically rotates certificates issued by trusted CA partners ie. DigiCert and GlobalSign. For Self-signed certificates and other CA certificates, you can set near expiry email notification.

* How to autorotate DigiCert Certificates?

	This would require you to add DigiCert to **Certificate Authorities** list. For the imported certificate, modify the **issuance policy** and **select CA** to be DigiCert. Modify the Lifetime action to **enable Auto-renewal**.

## **Recommended Documents**

* [Creating Certificate using CLI](https://docs.microsoft.com/rest/api/keyvault/createcertificate/createcertificate)
* [Setting Certificate Issuer using CLI](https://docs.microsoft.com/rest/api/keyvault/setcertificateissuer/setcertificateissuer)
* [About Azure Key Vault certificates](https://docs.microsoft.com/azure/key-vault/certificates/about-certificates)
