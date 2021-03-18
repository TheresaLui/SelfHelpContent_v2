<properties
  pagetitle="Integrating Key vault with Certificate Authority&#xD;"
  service="microsoft.keyvault"
  resource="vaults"
  ms.author="sebansal"
  selfhelptype="Generic"
  supporttopicids="32742806"
  resourcetags="optional"
  productpesids="15657"
  cloudenvironments="blackforest,fairfax,public,mooncake,usnat,ussec"
  articleid="keyvault-integratingkvwithca"
  ownershipid="AzureKeyVault_KeyVault" />
# Integrating Key vault with Certificate Authority
## **Recommended Steps**

* [Integrating Key Vault with DigiCert Certificate Authority](https://docs.microsoft.com/azure/key-vault/certificates/how-to-integrate-certificate-authority)
* [Getting pending request - status is "inProgress" or "canceled" or "failed"](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-scenarios)


### **Troubleshooting**

* I created a certificate from DigiCert. But it is failing/processing?
	
	Click on **Certificate Operations** tab of the certificate to view the error. If the error message advises you to contact DigiCert, then do so.

* New certificates show up in a disabled state, why?

	The certificate status changes after the CA signs the request. Check the progress after a certain amount of time. if it is not enabled, then it is likely that your request failed or was rejected by the CA.

* How to autorotate DigiCert Certificates?

	This would require you to add DigiCert to **Certificate Authorities** list. For the imported certificate, modify the **issuance policy** and **select CA** to be DigiCert. Modify the Lifetime action to **enable Auto-renewal**.

## **Recommended Documents**

* [Creating Certificate using CLI](https://docs.microsoft.com/rest/api/keyvault/createcertificate/createcertificate)
* [Setting Certificate Issuer using CLI](https://docs.microsoft.com/rest/api/keyvault/setcertificateissuer/setcertificateissuer)
* [About Azure Key Vault certificates](https://docs.microsoft.com/azure/key-vault/certificates/about-certificates)
