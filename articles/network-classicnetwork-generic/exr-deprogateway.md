<properties
    pageTitle="De-provisioning Issues - ExpressRoute Gateway"
    description="De-provisioning Issues - ExpressRoute Gateway"
    service="microsoft.network"
    resource="expressroutecircuits"
    authors="v-miegge"
    ms.author="v-miegge"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32627991"
    resourceTags=""
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="7dc6f9c7-df83-4ec6-8048-bbccfbde7bc3"
	ownershipId="CloudNet_AzureExpressRoute"
/>

# De-provisioning Issues - ExpressRoute Gateway

## Connectivity to Azure Private, Azure Public, or Dynamics 365 Services

## **Recommended Steps**

You can delete your ExpressRoute circuit by selecting the delete icon. Please note the following information:

* You must unlink all virtual networks from the ExpressRoute circuit
* You or your service provider must delete all the BGP Peerings on the circuit
* If the ExpressRoute circuit service provider provisioning state is Provisioning or Provisioned, you must work with your service provider to de-provision the circuit on their side
* If the service provider has de-provisioned the circuit (the service provider provisioning state is set to **Not Provisioned**), you can delete the circuit. This stops billing for the circuit.

## **Recommended Documents**

* [Remove a gateway](https://docs.microsoft.com/azure/expressroute/expressroute-howto-add-gateway-resource-manager#remove-a-gateway)<br>
* [De-provision and delete](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-portal-resource-manager#delete) an ExpressRoute circuit<br>
* [ExpressRoute Circuit Provisioning Workflow](https://docs.microsoft.com/azure/expressroute/expressroute-workflows)
