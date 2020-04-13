<properties
pageTitle="My Application Gateway has a missing listener."
description="My Application Gateway has a missing listener."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
ms.author="chadmat"
displayOrder="10"
articleId="AppGwNoHttpListenersFoundInsight"
diagnosticScenario="AppGwNoHttpListenersFoundInsight"
selfHelpType="Diagnostics"
supportTopicIds="32436961,32573483,32582834,32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Microsoft Azure has identified that your Application Gateway is missing a 'Http Listener'

<!--issueDescription-->
We have identified that your Application Gateway: **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->** has no Http Listener configured for Frontend port: **<!--$FrontEndPort-->[FrontEndPort]<!--/$FrontEndPort-->**, protocol: **<!--$Protocol-->[Protocol]<!--/$Protocol-->** Frontend IP: **<!--$FrontEndIp-->[FrontEndIp]<!--/$FrontEndIp-->**.
<!--/issueDescription-->

## **Recommended Steps**

1. Go to the [Azure Portal](https://portal.azure.com)
2. Find your Application Gateway, **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->**
3. Configure a new Http listener for port: **<!--$FrontEndPort-->[FrontEndPort]<!--/$FrontEndPort-->**, protocol: **<!--$Protocol-->[Protocol]<!--/$Protocol-->**, Frontend IP: **<!--$FrontEndIp-->[FrontEndIp]<!--/$FrontEndIp-->**
