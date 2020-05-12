<properties 
    pageTitle="End-to-end SSL issues"
    description="End-to-end SSL is not working properly"	
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    displayOrder="24"
    selfHelpType="resource"
    articleId="application-gateway-end-to-end-ssl"
	resourceTags=""
	productPesIds="15922"
    supportTopicIds="32582825"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# End-to-end SSL issues with Application Gateway

## **Recommended Steps**

If you are observing issues with End-to-end SSL encryption with Application Gateway, verify that:

1. **Protocol is HTTPS**: Ensure HTTPS is the protocol in both **listener** and **HTTP Settings** to enable end-to-end SSL
2. **Backend is known**: Application gateway only communicates with trusted backend instances in case of encrypted communication. A backend is trusted by default, if it is a trusted Azure service such as Azure app service, Azure API Management, etc, or the root certificate of the backend instance's certificate is from a well known CA. For other backend types, verify that you have explicitly added a certificate (trusted root certificate for V2 SKU and authentication certificate for V1 SKU) on the Application Gateway to [whitelist the backend](https://docs.microsoft.com/azure/application-gateway/end-to-end-ssl-portal#whitelist-certificates-for-backend-servers-1). 

## **Recommended Documents**

- [End-to-end SSL overview](https://docs.microsoft.com/azure/application-gateway/ssl-overview#end-to-end-ssl-encryption)
- [Configure end-to-end SSL with Application Gateway](https://docs.microsoft.com/azure/application-gateway/end-to-end-ssl-portal)
- [Generate certificates for whitelisting backend with Application Gateway](https://docs.microsoft.com/azure/application-gateway/certificates-for-backend-authentication)
- [Generate a self-signed certificate](https://docs.microsoft.com/azure/application-gateway/self-signed-certificates)
