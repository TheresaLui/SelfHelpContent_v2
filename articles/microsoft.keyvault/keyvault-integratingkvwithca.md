<properties
	pageTitle="Integrating Key vault with Certificate Authority"
	description="Integrating Key vault with Certificate Authority"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="sebansal"
	ms.author="sebansal"
	displayOrder="19"
	selfHelpType="generic"
	supportTopicIds="32742806"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-integratingkvwithca"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Integrating Key vault with Certificate Authority
## **Recommended Steps**

* [Integrating Key Vault with DigiCert Certificate Authority](https://docs.microsoft.com/azure/key-vault/certificates/how-to-integrate-certificate-authority)
* [Monitor and manage certificate creation](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-scenarios)


### **Troubleshooting**

* I created a certificate from DigiCert. But it is failing/processing?
	
	Click on **Certificate Operations** tab of the certificate to view the error. If the error message guides to contact DigiCert, then do so.

* New certificates show up in a disabled state, why?

	The certificate status changes after the CA signs the request. Check the progress after sometime, if it is never enabled, then it is likely that your request failed or was rejected by the CA.

* How to autorotate DigiCert Certificates?

	This would require you to add DigiCert to **Certificate Authorities** list. For the imported certificate, modify the **issuance policy** and **select CA** to be DigiCert. Modify the Lifetime action to **enable Auto-renewal**.

## **Recommended Documents**

* [Creating Certificate using CLI](https://docs.microsoft.com/rest/api/keyvault/createcertificate/createcertificate)
* [Setting Certificate Issuer using CLI](https://docs.microsoft.com/rest/api/keyvault/setcertificateissuer/setcertificateissuer)
* [About Azure Key Vault certificates](https://docs.microsoft.com/azure/key-vault/certificates/about-certificates)
