<properties
pageTitle="The Application Gateway frontend IPs are mismatched."
description="The Application Gateway frontend IPs are mismatched."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
ms.author="chadmat"
displayOrder="10"
articleId="AppGwFrontEndIpMismatch"
diagnosticScenario="AppGwFrontEndIpMismatch"
selfHelpType="Diagnostics"
supportTopicIds="32436961,32573483,32582834,32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Microsoft Azure has identified that your Application Gateway has a mismatched frontend IP address

<!--issueDescription-->
We have identified that your Application Gateway **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'** with the IP address in the URL **'<!--$UrlHost-->[UrlHost]<!--/$UrlHost-->'** does not match the **'<!--$FrontEndType-->[FrontEndType]<!--/$FrontEndType-->'** IP of the Frontend IP **'<!--$FrontEndIP-->[FrontEndIp]<!--/$FrontEndIp-->'**. This may be normal if a DNS CNAME or Azure Traffic Manager is being used to direct traffic to the Application Gateway IP address.

<!--/issueDescription-->

## **Recommended Steps**

If you are **NOT** using a DNS CNAME or Azure Traffic Manager, ensure that the host '<!--$UrlHost-->[UrlHost]<!--/$UrlHost-->' will eventually resolve to the IP '<!--$FrontEndIP-->[FrontEndIp]<!--/$FrontEndIp-->'. To validate the host to IP resolution, do the following:

1. Open a command prompt
2. Type `nslookup`
3. Type the host '<!--$UrlHost-->[UrlHost]<!--/$UrlHost-->'
4. Validate the returned IP is your Application Gateway Frontend IP of '<!--$FrontEndIP-->[FrontEndIp]<!--/$FrontEndIp-->'
5. If it does not resolve to the correct IP, update your DNS registration at your registrar
