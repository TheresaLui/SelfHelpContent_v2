<properties
pageTitle="NSGonGatewaySubnet"
description="NSGonGatewaySubnet"
infoBubbleText="Issues with Gateway Subnet detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
displayOrder=""
articleId="NSGonGatewaySubnet"
diagnosticScenario="NSGonGatewaySubnet"
selfHelpType="diagnostics"
supportTopicIds="32584253"
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="public"
/>
# We ran diagnostics on your virtual network and found an issue.
<!--issueDescription-->
Microsoft Azure has identified that the following [Subnet](data-blade:Microsoft_Azure_Network.VirtualNetworkSubnetsBlade): <!--$GatewaySubnet-->[GatewaySubnet]<!--/$GatewaySubnet--> has a Network Security Group associated to it.
This NSG must be deleted or disassociated with this subnet.
<!--/issueDescription-->

## **Recommended steps**
To resolve the most common issues, try one or more of the following methods.

1. When working with gateway subnets, avoid associating a network security group (NSG) to the gateway subnet. Associating a network security group to this subnet may cause your VPN gateway to stop functioning as expected. For more information about network security groups, see What is a [network security group?](https://docs.microsoft.com/azure/virtual-network/security-overview)

2. To resolve you issue, remove the NSG associated with your GatewaySubnet. To do this, navigate to the [Subnet](data-blade:Microsoft_Azure_Network.VirtualNetworkSubnetsBlade): <!--$GatewaySubnet-->[GatewaySubnet]<!--/$GatewaySubnet-->. Select the GatewaySubnet, click on Network Security group and select None in the Azure Portal.
<br>

## **Recommended steps**
[VPN Gateway FAQ](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq)
