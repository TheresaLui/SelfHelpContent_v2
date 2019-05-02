<properties 
    pageTitle="SSL termination issues"
    description="SSL termination is not working properly"
    infoBubbleText="SSL termincation issues with Application Gateway"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    selfHelpType="diagnostics"
    articleId="application-gateway-ssl-termination-insight"
    diagnosticScenario="ApplicationGatewaySSLTermiationIssues"
    supportTopicIds="32582828"
	productPesIds="15922"
    cloudEnvironments="public"
 />

# SSL termination issues with Application Gateway

We ran several diagnostic checks on your resource **<!--$ImpactedResource-->[ImpactedResource]<!--/$ImpactedResource-->**.  See the status of the diagnostic checks below.

## **Diagnostic checks executed**

* Check for <!--$NoHTTPSListenerFoundDisplayName-->[NoHTTPSListenerFoundDisplayName]<!--/$NoHTTPSListenerFoundDisplayName--> - <!--$NoHTTPSListenerFoundCheckStatus-->[NoHTTPSListenerFoundCheckStatus]<!--/$NoHTTPSListenerFoundCheckStatus-->
* Check for <!--$NoSSLCertificateFoundDisplayName-->[NoSSLCertificateFoundDisplayName]<!--/$NoSSLCertificateFoundDisplayName--> - <!--$NoSSLCertificateFoundCheckStatus-->[NoSSLCertificateFoundCheckStatus]<!--/$NoSSLCertificateFoundCheckStatus-->
* Check for  <!--$SSLCertificateExpiredDisplayName-->[SSLCertificateExpiredDisplayName]<!--/$SSLCertificateExpiredDisplayName--> - <!--$SSLCertificateExpiredCheckStatus-->[SSLCertificateExpiredCheckStatus]<!--/$SSLCertificateExpiredCheckStatus-->
* Check for  <!--$SSLCertificateNotYetValidDisplayName-->[SSLCertificateNotYetValidDisplayName]<!--/$SSLCertificateNotYetValidDisplayName--> - <!--$SSLCertificateNotYetValidCheckStatus-->[SSLCertificateNotYetValidCheckStatus]<!--/$SSLCertificateNotYetValidCheckStatus-->
* Check for  <!--$SNINotFoundDisplayName-->[SNINotFoundDisplayName]<!--/$SNINotFoundDisplayName--> - <!--$SNINotFoundCheckStatus-->[SNINotFoundCheckStatus]<!--/$SNINotFoundCheckStatus-->

## **Recommended Steps**

Check the status of each diagnostic check mentioned above. Use the below links to troubleshoot issues with those diagnostic checks which have been flagged as 'failed'.

* **No HTTP listener found**: This implies that you have not configured SSL termination on the listener which is accepting the request. See [configure SSL termination](https://docs.microsoft.com/azure/application-gateway/create-ssl-portal) and configure the listener accordingly.
* **No SSL certificate found**: You need to add SSL certificate to the listener to enable the application gateway to derive a symmetric key to perform SSL termination. See [add SSL certificate](https://docs.microsoft.com/azure/application-gateway/create-ssl-portal#create-an-application-gateway) to add the required certificate to the listener.
- **SSL certificate expired**: This implies that the current date and time is outside the "Valid from" and "Valid to" date range on the certificate. Renew the certificate and then update it in the Application Gateway.
- **SSL certificate not yet valid**: This implies that the certificate is not yet valid. Either renew the certificate or wait till the "Valid from" date to use the certificate for SSL termination.
- **SNI is enabled**: Since you've enabled SNI on the listener, you need to ensure that the client also supports SNI (Server Name Indication).
