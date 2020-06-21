<properties
pageTitle="Application Gateway has a NSG on the subnet"
description="Application Gateway has a NSG on the subnet"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="ApplicationGatewayhasaNSGonthesubnet"
diagnosticScenario="ApplicationGatewayhasaNSGonthesubnet"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Application Gateway Subnet Has NSG Applied
<!--issueDescription-->
We have identified that your Application Gateway: **<!--$GatewayName-->[GatewayName]<!--/$GatewayName-->** in Subnet: **<!--$SubnetName-->[SubnetName]<!--/$SubnetName-->** has the following NSG associated: **<!--$NSGName-->[NSGName]<!--/$NSGName-->**. If the NSG has not been carefully configured health probe traffic from the Application Gateway can be blocked from reaching the backend resources. This will cause the Application Gateway to mark the backend resources as unhealthy and not route traffic to them. NSGs can also block legitimate traffic coming from the Application Gateway causing issues with the solution hosted on by the backend resources as well as diagnostic logging disruptions. 
<!--/issueDescription-->
## **Steps to resolve the issue**

1. [Delete the NSG](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group#delete-a-network-security-group) from the Application Gateway subnet and test communication.
2. If a NSG is required, follow the directions at [Can I whitelist Application Gateway access to a few source IPs?](https://docs.microsoft.com/azure/application-gateway/application-gateway-faq) in the FAQ.
