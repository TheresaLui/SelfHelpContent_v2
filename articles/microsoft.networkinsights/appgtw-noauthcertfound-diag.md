<properties
pageTitle="No authentication certificate found for my Application Gateway."
description="No authentication certificate found for my Application Gateway."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="AppGwAuthenticationCertificateNotFound"
diagnosticScenario="AppGwAuthenticationCertificateNotFound"
selfHelpType="Diagnostics"
supportTopicIds="32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public"
/>
# Microsoft Azure had identified that your Application Gateway is missing an authentication certificate
<!--issueDescription-->
We have identified that your Application Gateway: **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->** has a backend Http setting **<!--$BackendHttpSettingName-->[BackendHttpSettingsName]<!--/$BackendHttpSettingName-->** of protocol HTTPS and has no Authentication Certificate configured. **If the backend is an Azure WebApp, this configuration is correct and no action is required.**
<!--/issueDescription-->
## **Steps to resolve**
If backend server is not an Azure Web App, the authentication certificate for backend server must be white-listed. Read more on [how to whitelist certificates](https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-ssl#end-to-end-ssl-and-whitelisting-of-certificates).