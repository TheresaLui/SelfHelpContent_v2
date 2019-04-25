<properties 
    pageTitle="End-to-end SSL issues"
    description="End-to-end SSL is not working properly"
    infoBubbleText="Common solution article for instructions on how to troubleshoot end-to-end-ssl issues with Application Gateway."	
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    selfHelpType="diagnostics"
    articleId="application-gateway-end-to-end-ssl"
    diagnosticScenario="ApplicationGatewayEndToEndSSLIssues"
    supportTopicIds="32582825"
    cloudEnvironments="public"
 />

# End-to-end SSL issues with Application Gateway

## **Recommended Steps**

If you are observing issues with End-to-end SSL encryption with Application Gateway, verify that:

1. **Protocol is HTTPS**-  You need to ensure HTTPS is the protocol in both listener and backend HTTP Settings to enable end-to-end SSL.
2. **Backend is whitelisted**- Application gateway only communicates with known backend instances that have either whitelisted their certificate with the application gateway or are trusted Azure service such as app service. See [certificate whitelisting consideration](https://docs.microsoft.com/azure/application-gateway/ssl-overview#end-to-end-ssl-and-whitelisting-of-certificates) to verify that you have whitelisted the backend.
3. **Certificate is valid**: For the end-to-end SSL encryption to work, you need to ensure that the certificates used in the listener as well as the HTTP Settings meet the following conditions:
   - That the current date and time is within the "Valid from" and "Valid to" date range on the certificate.
   - That the certificate's "Common Name" (CN) matches the host header in the request. For example, if the client is making a request to `https://www.contoso.com/`, then the CN must be `www.contoso.com`.

## **Recommended Documents**

- [End-to-end SSL overview](https://docs.microsoft.com/azure/application-gateway/ssl-overview#end-to-end-ssl-encryption).
- [Configure end-to-end SSL with Application Gateway](https://docs.microsoft.com/azure/application-gateway/end-to-end-ssl-portal).