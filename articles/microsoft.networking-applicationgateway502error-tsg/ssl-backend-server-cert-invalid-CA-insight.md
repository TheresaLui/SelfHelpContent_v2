<properties
pageTitle="Application Gateway 502 Error: Backend Server Certificate Invalid CA Insight"
description="Application Gateway 502 Error: Backend Server Certificate Invalid CA Insight"
infoBubbleText= "Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="applicationGateway"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="9b0ae114-f24c-4d34-974b-8a4d718c0df6"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway 502 Error: Backend Server Certificate Invalid CA Insight

<!--issueDescription-->
End-to-End SSL with Application Gateway v2 requires the backend server’s certificate to be verified to deem the server healthy. For an SSL certificate to be trusted, that certificate of the backend server must have been issued by a CA that is included in the trusted store of the Application Gateway. If the certificate was not issued by a trusted CA, for example, self-signed certificates, users should upload the issuer’s certificate to Application Gateway. To resolve this, please extract the root certificate of the backend server certificate and upload it to the Application Gateway’s respective HTTP Settings
<!--/issueDescription-->
