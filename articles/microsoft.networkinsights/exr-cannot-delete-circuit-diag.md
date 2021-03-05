<properties
pageTitle="Cannot Delete ExpressRoute Circuit"
description="Provides the solution to the problem in which you cannot delete ExpressRoute Circuit"
infoBubbleText="Issues with your ExpressRoute were detected. See details on the right."
service="microsoft.network"
resource="ExpressRoute"
authors="genlin"
ms.author="mariliu"
articleId="CannotDeleteExpressRouteCircuit"
selfHelpType="Diagnostics"
resourceTags="windows"
supportTopicIds="32627989"
productPesIds="15480"
cloudEnvironments="Public, fairfax, usnat, ussec"
ownershipId="CloudNet_AzureExpressRoute"
/>

# Cannot delete ExpressRoute circuit
<!--issueDescription-->
We have determined that the ExpressRoute circuit **<!--$CircuitName-->CircuitName<!--/$CircuitName-->** cannot be deleted because it has associated virtual network connections. ExpressRoute facilitates connectivity to private resources deployed within an Azure virtual network via private peering or to online Microsoft resources deployed with a public IP address via Microsoft peering. To delete an ExpressRoute circuit, any reference resources (such as Route Filters or virtual network connections) must be deleted and any peering must be deprovisioned.

Here is the list of virtual network connections to the circuit **<!--$CircuitName-->CircuitName<!--/$CircuitName-->**:

**<!--$list-->list<!--/$list-->**
<!--/issueDescription-->

## **Recommended Steps**

- Delete any route filters associated with the target ExpressRoute circuit.
- Delete the connections and authorizations that are associated with the circuit. If a connection belongs to a different subscription, or if an authorization is in use by another subscription, contact the subscription owner for more help.
- Deprovision private peering.
- Deprovision Microsoft peering.
- If you're using the ExpressRoute partner model, the ExpressRoute partner must deprovision the connection on their end and update the circuit status. Please work directly with your ExpressRoute partner to complete this step.

## **Recommended Documents**

How to remove virtual network links:

- [Portal instructions](https://docs.microsoft.com/azure/expressroute/expressroute-howto-linkvnet-portal-resource-manager#clean-up-resources) 
- [PowerShell for ARM VNets](https://docs.microsoft.com/azure/expressroute/expressroute-howto-linkvnet-arm#clean-up-resources)
- [PowerShell for classic VNets](https://docs.microsoft.com/azure/expressroute/expressroute-howto-linkvnet-classic#remove-a-virtual-network-link-to-a-circuit)
