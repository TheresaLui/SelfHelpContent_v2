<properties
pageTitle="The Application Gateway certificate is not valid."
description="The Application Gateway certificate is not valid."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="AppGwAuthenticationCertificateExpiredInsight"
diagnosticScenario="AppGwAuthenticationCertificateExpiredInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Microsoft Azure has identified an issue with your Application Gateway authentication certificate
<!--issueDescription-->
We have identified that your Application Gateway, **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'**, has an authentication certificate, **'<!--$AuthCertificate-->[AuthCertName]<!--/$AuthCertificate-->'** that is not valid after date: **<!--$Timestamp-->[NotAfter]<!--/$Timestamp-->**.  This certificate cannot be used for authentication as the expiration date has been reached.
<!--/issueDescription-->
## **Recommended Steps**
To resolve this issue upload a new 'Authentication Certificate' in the https listener blade in the [Azure portal](https://portal.azure.com) or PowerShell, whichever you are more comfortable with. The step-by-step instructions are found [here](https://docs.microsoft.com/azure/application-gateway/renew-certificates).
