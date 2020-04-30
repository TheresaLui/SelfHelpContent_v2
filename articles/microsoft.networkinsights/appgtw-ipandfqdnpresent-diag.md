<properties
pageTitle="My Application Gateway backendpool has both IP addresses and FQDN."
description="My Application Gateway backendpool has both IP addresses and FQDN."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
ms.author="chadmat"
displayOrder="10"
articleId="AppGwBackendAddressPoolIpAndFdqn"
diagnosticScenario="AppGwBackendAddressPoolIpAndFdqn"
selfHelpType="Diagnostics"
supportTopicIds="32436961,32573483,32582834,32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Microsoft Azure has identified an issue with your Application Gateway's backend address pool

<!--issueDescription-->
We have identified that your Application Gateway: **<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'s** backend address pool, **<!--$BackendAddressPool-->[BackendAddressPool]<!--/$BackendAddressPool-->**, contains IP Addresses and FQDNs. This could be an issue if the **<!--$BackendAddressPool-->[BackendAddressPool]<!--/$BackendAddressPool-->** is using HTTPS as the resources with IP addresses will fail due to a subject name mismatch when validating the SSL certificate.
<!--/issueDescription-->

## **Recommended Steps**

1. Open the [Azure Portal](https://portal.azure.com)
2. Go to your Application Gateway **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->'**
3. Go to the 'Backend pools' blade and choose **<!--$BackendAddressPool-->[BackendAddressPool]<!--/$BackendAddressPool-->**
4. Select the associated rule
5. Select the HTTP setting
6. If it is utilizing HTTPS, update the 'Host Name' field to have FQDNs so HTTPS will succeed
