<properties
	pageTitle="Configure SSL and Authentication/Trusted Root Certificates"
	description="Configure SSL and Authentication/Trusted Root Certificates"
	service="microsoft.network"
	resource="applicationgateways"
	authors="surajmb"
	ms.author="surmb"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639109"
	resourceTags=""
	productPesIds="15922"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="configure-ssl-auth-trustedrootcert"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Configure SSL and Authentication/Trusted Root Certificates
For SSL Offload or End to End SSL, Application Gateway requires you to upload an SSL certificate in the PFX format to the HTTP Listener or in the V2 SKU, you have the option to use KeyVault to refer your certificates in the listener.

To perform end to end SSL, Application Gateway requires the backend instances to be whitelisted by uploading authentication/trusted root certificates. In case of v1 SKU, authentication certificates are required whereas in case of v2 SKU, trusted root certificates are required for whitelisting the certificates

## **Recommended Documents**

* [Create certificates for whitelisting backend](https://docs.microsoft.com/azure/application-gateway/certificates-for-backend-authentication) with Azure Application Gateway
* [Renewing SSL Certificates](https://docs.microsoft.com/azure/application-gateway/renew-certificates) in Application Gateway
* [Using Azure KeyVault](https://docs.microsoft.com/azure/application-gateway/key-vault-certs)
* Configure SSL termination with Azure KeyVault using [Azure PowerShell](https://docs.microsoft.com/azure/application-gateway/configure-keyvault-ps)
* [Generate a self-signed certificate](https://docs.microsoft.com/azure/application-gateway/self-signed-certificates)
