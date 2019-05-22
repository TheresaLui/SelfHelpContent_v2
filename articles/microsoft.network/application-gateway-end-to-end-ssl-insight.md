<properties 
    pageTitle="End-to-end SSL issues"
    description="End-to-end SSL is not working properly"
    infoBubbleText="End-to-end SSL issues with Application Gateway"
    service="microsoft.network"
    resource="applicationgateways"
    authors="abshamsft"
    ms.author="absha"
    selfHelpType="diagnostics"
    articleId="application-gateway-end-to-end-ssl-insight"
    diagnosticScenario="ApplicationGatewayEndToEndSSLIssues"
    supportTopicIds="32582825"
	productPesIds="15922"
    cloudEnvironments="public"
 />

# End-to-end SSL issues with Application Gateway

We ran several diagnostic checks on your resource **<!--$ImpactedResource-->[ImpactedResource]<!--/$ImpactedResource-->**. See the status of the diagnostic checks below.

## **Diagnostic checks executed**

* Check for <!--$NoHTTPSSettingFoundDisplayName-->[NoHTTPSSettingFoundDisplayName]<!--/$NoHTTPSSettingFoundDisplayName--> - <!--$NoHTTPSSettingFoundCheckStatus-->[NoHTTPSSettingFoundCheckStatus]<!--/$NoHTTPSSettingFoundCheckStatus-->
* Check for <!--$NoAuthenticationCertificateFoundDisplayName-->[NoAuthenticationCertificateFoundDisplayName]<!--/$NoAuthenticationCertificateFoundDisplayName--> - <!--$NoAuthenticationCertificateFoundCheckStatus-->[NoAuthenticationCertificateFoundCheckStatus]<!--/$NoAuthenticationCertificateFoundCheckStatus-->
* Check for  <!--$AuthenticationCertificateExpiredDisplayName-->[AuthenticationCertificateExpiredDisplayName]<!--/$AuthenticationCertificateExpiredDisplayName--> - <!--$AuthenticationCertificateExpiredCheckStatus-->[AuthenticationCertificateExpiredCheckStatus]<!--/$AuthenticationCertificateExpiredCheckStatus-->
* Check for  <!--$AuthenticationCertificateNotYetValidDisplayName-->[AuthenticationCertificateNotYetValidDisplayName]<!--/$AuthenticationCertificateNotYetValidDisplayName--> - <!--$AuthenticationCertificateNotYetValidCheckStatus-->[AuthenticationCertificateNotYetValidCheckStatus]<!--/$AuthenticationCertificateNotYetValidCheckStatus-->
* Check for  <!--$NoTrustedRootCertificateFoundDisplayName-->[NoTrustedRootCertificateFoundDisplayName]<!--/$NoTrustedRootCertificateFoundDisplayName--> - <!--$NoTrustedRootCertificateFoundCheckStatus-->[NoTrustedRootCertificateFoundCheckStatus]<!--/$NoTrustedRootCertificateFoundCheckStatus-->
* Check for  <!--$TrustedRootCertificateExpiredDisplayName-->[TrustedRootCertificateExpiredDisplayName]<!--/$TrustedRootCertificateExpiredDisplayName--> - <!--$TrustedRootCertificateExpiredCheckStatus-->[TrustedRootCertificateExpiredCheckStatus]<!--/$TrustedRootCertificateExpiredCheckStatus-->
* Check for  <!--$TrustedRootCertificateNotYetValidDisplayName-->[TrustedRootCertificateNotYetValidDisplayName]<!--/$TrustedRootCertificateNotYetValidDisplayName--> - <!--$TrustedRootCertificateNotYetValidCheckStatus-->[TrustedRootCertificateNotYetValidCheckStatus]<!--/$TrustedRootCertificateNotYetValidCheckStatus-->

## **Recommended Steps**

Check the status of each diagnostic check mentioned above. Use the below links to troubleshoot issues with those diagnostic checks which have been flagged as 'failed'.

* **Protocol is not HTTPS in backend HTTP Settings**: This implies that you have chosen HTTP as the protocol instead of HTTPS in the backend HTTP Settings associated with this listener. You need to select HTTPS as the protocol in both listener and backend HTTP Settings to enable end-to-end SSL.
* **No authentication certificate found**: You need to add authentication certificate to the backend HTTP Settings to enable the application gateway to whitelist the backend to perform end-to-end SSL. See [whitelist certificates for backend servers](https://docs.microsoft.com/azure/application-gateway/end-to-end-ssl-portal#whitelist-certificates-for-backend-servers-1) to add the required certificates.
* **Authentication certificate expired**: This implies that the current date and time is outside the "Valid from" and "Valid to" date range on the certificate. Renew the certificate and then update it in the Application Gateway.
* **Authentication certificate not yet valid**: This implies that the certificate is not yet valid. Either renew the certificate or wait till the "Valid from" date to use the certificate for whitelisting the backend servers.

If the above steps do not resolve the issue, then verify that you have configured end-to-end SSL correctly. See how to [configure end-to-end SSL with Application Gateway](https://docs.microsoft.com/azure/application-gateway/end-to-end-ssl-portal).
