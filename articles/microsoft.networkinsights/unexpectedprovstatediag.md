<properties 
pageTitle="UnexpectedProvState" 
description="UnexpectedProvStateDiag"
infoBubbleText="The Express Route Circuit is in an Unexpected Provisioning State.  See details on right." 
service="microsoft.network" 
resource="ExpressRoute" 
authors="KristinaNeyens" 
displayOrder="" 
articleId="ExRCircuitProvisioningStateInsight" 
diagnosticScenario="UnexpectedProvState"
selfHelpType="diagnostics"
supportTopicIds="32539943, 32586802"
resourceTags="windows" 
productPesIds="15480" 
cloudEnvironments="public, Fairfax, usnat, ussec" 
	ownershipId="CloudNet_AzureExpressRoute"
/> 
# Express Route Circuit Diagnostic Result 
Azure has run diagnostics and found an issue:  the circuit is in an "Unexpected" Provisioning State.  Provisioning an ExpressRoute circuit establishes a Layer 2 connection.  In the ExpressRoute Essentials blade, the "Circuit Status must be "Enabled" and the Provider Status "Provisioned" in order to be used.

## Below is a list of potential items to check (and rectify): <br> 
1. The peer address might be overlapped with the Vnet address prefix
2. There is a default route configured in the route table
3. There may be a circuit capacity issue, or not enough physical capacity on the port pair
4. The NAT pool has no resources left
5. If attempting to delete/deprovision a circuit, a virtual network may still be linked to the circuit.  Unlink all virtual networks from the ExpressRoute circuit for the delete operation to succeed
6. If attempting to delete/deprovision a circuit and the circuit service provider provisioning state is 'Provisioning' or 'Provisioned', you must work 
with your service provider to deprovision the circuit on their side. Once the service provider has deprovisioned the circuit 
(the service provider provisioning state is set to Not Provisioned), you can delete the circuit. This stops billing for the circuit.

Reference link:
[Deprovisioning and deleting an ExpressRoute circuit](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-portal-resource-manager#delete)
