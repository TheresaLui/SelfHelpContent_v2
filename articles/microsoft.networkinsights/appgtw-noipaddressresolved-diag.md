<properties
pageTitle="My Application Gateway has No IP Address Resolved"
description="My Application Gateway has No IP Address Resolved"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="Parag"
displayOrder="10"
articleId="AppGwChecklistNoIPAddressResolved"
diagnosticScenario="AppGwChecklistNoIPAddressResolved"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Application Gateway Diagnostic Result
<!--issueDescription-->
Microsoft Azure has identified Application Gateway: 
The host <!--$HostUrl-->[HostUrl]<!--/$HostUrl--> does not resolve to any IP Address.
<!--/issueDescription-->
## **Steps to resolve this issue**
Make sure DNS records are configured correctly for the host <!--$HostUrl-->[HostUrl]<!--/$HostUrl-->. In case this is a private frontend, make sure that the DNS server is able to resolve the host correctly.