<properties
pageTitle="Application Gateway has a UDR on the subnet"
description="Application Gateway has a UDR on the subnet"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="ApplicationGatewayhasaUDRonthesubnet"
diagnosticScenario="ApplicationGatewayhasaUDRonthesubnet"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Application Gateway Subnet Has User-defined Route Applied
<!--issueDescription-->
We have identified that your Application Gateway: **<!--$GatewayName-->[GatewayName]<!--/$GatewayName-->** in Subnet: **<!--$SubnetName-->[SubnetName]<!--/$SubnetName-->** has the following User-defined Route (UDR) associated: **<!--$UDRName-->[UDRName]<!--/$UDRName-->**. If the UDR has not been carefully configured, health probe traffic from the Application Gateway can be rerouted and will not reach the backend resources. This will cause the Application Gateway to mark the backend resources as unhealthy and not route traffic to them. UDRs can also reroute legitimate traffic coming from the Application Gateway causing issues with the solution hosted by the backend resources. 
<!--/issueDescription-->
## **Steps to resolve the issue**

1. [Delete the UDR](https://docs.microsoft.com/azure/virtual-network/manage-route-table#delete-a-route-table) from the Application Gateway subnet and test communication.
2. If a UDR is required, follow the directions at [Are user-defined routes supported on the application gateway subnet?](https://docs.microsoft.com/azure/application-gateway/application-gateway-faq) in the FAQ.
