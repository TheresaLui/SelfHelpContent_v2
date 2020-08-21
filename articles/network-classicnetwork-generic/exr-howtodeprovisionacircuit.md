<properties
	pageTitle="management/how to de-provision a circuit"
	description="management/how to de-provision a circuit"
	service="microsoft.network"
	resource="expressroutecircuits"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32586809"
	resourceTags=""
	productPesIds="15480"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="15f58cef-f0a4-4fe8-a5b4-f294fa130154"
	ownershipId="CloudNet_AzureExpressRoute"
/>

# managment/how to de-provision a circuit
## **Recommended steps**
You can delete your ExpressRoute circuit by selecting the delete icon. Note the following information:<br>
1. You must unlink all virtual networks from the ExpressRoute circuit.<br>
2. If the ExpressRoute circuit service provider provisioning state is Provisioning or Provisioned you must work with your service provider to deprovision the circuit on their side.<br>
3. If the service provider has deprovisioned the circuit (the service provider provisioning state is set to Not provisioned), you can delete the circuit. This stops billing for the circuit.

## **Recommended documents**
[De-provision and delete an ExpressRoute circuit](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-portal-resource-manager#delete)
