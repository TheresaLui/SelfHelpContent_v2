<properties
	pageTitle="Managing Certificates in Key Vault"
	description="Managing Certificates in Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="sebansal"
	displayOrder="5"
	selfHelpType="generic"
	supportTopicIds="32738118"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-certificatehowother"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Managing Certificates in Key Vault
## **Recommended Steps**

* [Storing App Service Certificate in Key Vault](https://docs.microsoft.com/azure/app-service/configure-ssl-certificate#import-an-app-service-certificate)
* [Web Service Certificate](https://azure.github.io/AppService/2016/05/24/Deploying-Azure-Web-App-Certificate-through-Key-Vault.html)

### **Troubleshooting**

*  **Error type 'The public key of the end-entity certificate in the specified X.509 certificate content does not match the public part of the specified private key. Please check if certificate is valid'**
	
	This error can occur if you are not merging the CSR with the same CSR request initiated. Each time a CSR is created, it creates a private key which has to be matched when merging the signed request.
* Unauthorized access, access denied, forbidden, or similar error: The principal used doesn't have access to the resource it's trying to access.

* I have accidentally **deleted a certificate**. How can i recover it?
	
	If the key vault had soft-deleted enabled, you can [recover deleted certificate](https://docs.microsoft.com/rest/api/keyvault/recoverdeletedcertificate), [view deleted certificate](https://docs.microsoft.com/rest/api/keyvault/getdeletedcertificate/getdeletedcertificate).

## **Recommended Documents**

* [Securely save secret application settings for a web](https://docs.microsoft.com/azure/key-vault/vs-secure-secret-appsettings)
* [Use the Key Vault Connected Service](https://docs.microsoft.com/azure/key-vault/vs-key-vault-add-connected-service)
