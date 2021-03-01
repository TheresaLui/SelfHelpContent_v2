<properties
pageTitle="Route propagation disabled on gateway subnet"
description="Provide the solution to a issue in which Route propagation is disabled on gateway subnet"
infoBubbleText="Issues with your Virtual Network Gateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="genlin"
ms.author="mariliu"
articleId="VNGVirtualNetworkGatewayUpgradeDetectedInsight"
selfHelpType="Diagnostics"
supportTopicIds = "32591151"
productPesIds="16094"
cloudEnvironments="Public, fairfax, usnat, ussec"
ownershipId="CloudNet_AzureVPNGateway"
/>

# Route propagation disabled on gateway subnet
<!--issueDescription-->
We has detected a route table that is attached to the gateway subnet has route propagation disabled.
The route propagation should not be disabled on the gateway subnet. The gateway will not function if this setting is disabled.
<!--/issueDescription-->

## **Recommended Steps**
To restore route propagation for the VPN gateway, follow these steps:

1. sign in to the Azure portal, and locate the affected route table.
2. On the **Configuration settings** blade, select **Yes** under **propagate gateway routes**.

## **Recommended Documents**

- [Route propagation should not be disabled](https://docs.microsoft.com/azure/virtual-network/virtual-networks-udr-overview#border-gateway-protocol)
- [Manage Route tables](https://docs.microsoft.com/azure/virtual-network/manage-route-table#create-a-route-table)


