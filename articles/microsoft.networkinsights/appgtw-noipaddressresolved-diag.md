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
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Application Gateway Diagnostic Result
<!--issueDescription-->
Microsoft Azure has identified Application Gateway: **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'** with the host <!--$HostUrl-->[HostUrl]<!--/$HostUrl--> that does not resolve to any IP Address.
<!--/issueDescription-->
## **Steps to resolve this issue**
Make sure DNS records are configured correctly for the host **<!--$HostUrl-->[HostUrl]<!--/$HostUrl-->**. In case this is a private frontend, make sure that the DNS server is able to resolve the host correctly.

1. In the Azure portal, navigate to the VNet your Application Gateway is associated with
2. Open the 'DNS Servers' blade and make note of the IPs
3. Log into the DNS servers and ping the host **<!--$HostUrl-->[HostUrl]<!--/$HostUrl-->**
4. Ensure the custom DNS servers are able to resolve all names in the backend address pool
