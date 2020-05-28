<properties 
    pageTitle="SSL termination issues"
    description="SSL termination is not working properly"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="26"
    selfHelpType="resource"
    articleId="application-gateway-ssl-termination"
	resourceTags=""
	productPesIds="15922"
    supportTopicIds="32582828"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# SSL termination issues with Application Gateway

## **Recommended Steps**

If you are observing issues with SSL termination with Application Gateway, verify that:

1. **Protocol is HTTPS**: Ensure HTTPS is the protocol in the listener which is accepting the HTTPS request
2. **Certificate is valid**: For the SSL termination to work, ensure that the certificate used in the listener meets the following conditions:

   - The current date and time is within the "Valid from" and "Valid to" date range on the certificate
   - The certificate's "Common Name" (CN) matches the host header in the request. For example, if the client is making a request to `https://www.contoso.com/`, then the CN must be `www.contoso.com`.

## **Recommended Documents**

- [SSL termination overview](https://docs.microsoft.com/azure/application-gateway/ssl-overview#ssl-termination)
- [Configure SSL termination with Application Gateway](https://docs.microsoft.com/azure/application-gateway/create-ssl-portal)
