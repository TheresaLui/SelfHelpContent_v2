<properties
pageTitle="Route propagation disabled on gateway subnet"
description="Provide the solution to a issue in which Route propagation is disabled on gateway subnet"
infoBubbleText="Issues with your Virtual Network Gateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="genlin"
ms.author="mariliu"
articleId="disableBgpRoutePropagationTrue"
selfHelpType="Diagnostics"
supportTopicIds = "32591151"
productPesIds="16094"
cloudEnvironments="Public, fairfax, usnat, ussec"
ownershipId="CloudNet_AzureVPNGateway"
/>

# Route propagation disabled on gateway subnet
<!--issueDescription-->
We detected a route table attached to the gateway subnet has **Route propagation** disabled.
The route propagation should not be disabled on the gateway subnet, or the gateway will not function.
<!--/issueDescription-->

## **Recommended Steps**
To enable route propagation for the VPN gateway, follow these steps:

1. Sign in to the Azure portal, and locate the affected route table.
2. On the **Configuration settings** blade, select **Yes** under **propagate gateway routes**.

## **Recommended Documents**

- [Route propagation should not be disabled](https://docs.microsoft.com/azure/virtual-network/virtual-networks-udr-overview#border-gateway-protocol)
- [Manage Route tables](https://docs.microsoft.com/azure/virtual-network/manage-route-table#create-a-route-table)


