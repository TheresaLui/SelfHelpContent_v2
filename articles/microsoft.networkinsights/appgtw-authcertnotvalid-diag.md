<properties
pageTitle="The Application Gateway certificate is not yet valid."
description="The Application Gateway certificate is not yet valid."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
ms.author="chadmat"
displayOrder="10"
articleId="AppGwAuthenticationCertificateNotYetValidInsight2"
diagnosticScenario="AppGwAuthenticationCertificateNotYetValidInsight"
selfHelpType="Diagnostics"
supportTopicIds="32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Microsoft Azure has identified an issue with your Application Gateway authentication certificate
<!--issueDescription-->
We have identified that your Application Gateway, **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'**, has an authentication certificate, **'<!--$AuthCertificate-->[AuthCertName]<!--/$AuthCertificate-->'** that is not valid before date: **<!--$Timestamp-->[NotBefore]<!--/$Timestamp-->**.  This certificate cannot be used for authentication until that date is reached.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue upload a new 'Authentication Certificate' in the https listener blade in the [Azure portal](https://portal.azure.com) or powershell, whichever you are more comfortable with. The step-by-step instructions are found [here](https://docs.microsoft.com/azure/application-gateway/renew-certificates).
