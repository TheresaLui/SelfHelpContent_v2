<properties
	pageTitle="Deprovisioning Issues"
	description="Deprovisioning Issues"
	service="microsoft.network"
	resource="expressroutecircuits"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32627990, 32627989, 32627992, 32627991, 32627993"
	resourceTags=""
	productPesIds="15480"
	cloudEnvironments="public"
	articleId="a69eee20-f1cb-4ef6-a3f4-a2ade648df86"
/>

# Connectivity to Azure Private, Azure Public, or Dynamics 365 Services

You can delete your ExpressRoute circuit by selecting the delete icon. Please note the following information:

1. You must unlink all virtual networks from the ExpressRoute circuit
2. You or your service provider must delete all the BGP Peerings on the circuit
3. If the ExpressRoute circuit service provider provisioning state is Provisioning or Provisioned, you must work with your service provider to deprovision the circuit on their side
4. If the service provider has deprovisioned the circuit (the service provider provisioning state is set to **Not Provisioned**), you can delete the circuit. This stops billing for the circuit.

## **Recommended Documents**

* [Deprovision and delete](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-portal-resource-manager#delete) an ExpressRoute circuit
