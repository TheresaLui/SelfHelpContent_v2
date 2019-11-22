<properties
pageTitle="Application Gateway 502 Error: Backend Server Certificate needs to be whitelisted Insight"
description="Application Gateway 502 Error: Backend Server Certificate needs to be whitelisted Insight"
infoBubbleText= "Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="applicationGateway"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="5b90a2c2-d59e-4691-a198-b3f8db6b2a8e"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public" />

# Application Gateway 502 Error: Backend Server Certificate needs to be whitelisted Insight

<!--issueDescription-->
<<<<<<< HEAD:articles/microsoft.networking-applicationgateway502error-tsg/ssl-backend-cert-needs-whitelisted-insight.md
Certificate uploaded in Application Gateway does not match with the certificate used by the backend server or the certificate might be invalid. To resolve this, check the certificate returned by the server when accessed directly and if there is a mismatch, upload it to the Application Gateway’s respective HTTP Settings. 

=======
Certificate uploaded in Application Gateway does not match with the certificate used by the backend server or the certificate might be invalid. To resolve this, check the certificate returned by the server when accessed directly and if there is a mismatch, upload it to the Application Gateway’s respective HTTP Settings.
>>>>>>> dde7a9686a82f38b5a843e15db14e833a6305b59:articles/microsoft.networking_applicationgateway502error_tsg/ssl-backend-cert-needs-whitelisted-insight.md
<!--/issueDescription-->

Check this [document](https://docs.microsoft.com/azure/application-gateway/certificates-for-backend-authentication) to learn more on how to export and upload authentication certificate in Application Gateway V1.
