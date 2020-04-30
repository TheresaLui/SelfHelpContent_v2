<properties
pageTitle="Application Gateway SSL Certificate Validity"
description="Application Gateway SSL Certificate Validity"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="Application Gateway"
authors="chadmath"
ms.author="karenha"
displayOrder="1"
articleId="AppGwChecklistNoSSLCertificateFound"
diagnosticScenario="AppGwChecklistNoSSLCertificateFound"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
ownershipId="CloudNet_AzureApplicationGateway"
/>
# Microsoft Azure has identified your Application Gateway listener has no valid SSL certificate configured
<!--issueDescription-->
We have identified that your Application Gateway, **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'**, has a HTTP listener **<!--$ListenerName-->[ListenerName]<!--/$ListenerName-->** of protocol HTTPS that has no SSL Certificate configured.
<!--/issueDescription-->
## **Steps to Update Expiring/Expired Certificates**
To resolve this issue upload a new 'SSL Certificate' in the Listeners blade in the [Azure portal](https://portal.azure.com) or PowerShell, whichever you are more comfortable with. The step-by-step instructions are found [here](https://docs.microsoft.com/azure/application-gateway/renew-certificates).
