<properties
	pageTitle="Deprovisioning ExpressRoute Direct"
	description="Deprovisioning ExpressRoute Direct"
	service="microsoft.network"
	resource="expressroutecircuits"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32627990, 32627989, 32627992, 32627991, 32627993"
	resourceTags=""
	productPesIds="15480"
	cloudEnvironments="public"
/>

# Connectivity to Azure Private, Azure Public or Dynamics 365 Services

You can delete your ExpressRoute circuit by selecting the delete icon. Note the following information:<br>
1. You must unlink all virtual networks from the ExpressRoute circuit.<br>
2. You or your service provider must delete all the BGP Peerings on the circuit.<br>
3. If the ExpressRoute circuit service provider provisioning state is Provisioning or Provisioned you must work with your service provider to deprovision the circuit on their side.<br>
4. If the service provider has deprovisioned the circuit (the service provider provisioning state is set to Not provisioned), you can delete the circuit. This stops billing for the circuit.<br>

## **Recommended documents**

[De-provision and delete](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-portal-resource-manager#delete) an ExpressRoute circuit
