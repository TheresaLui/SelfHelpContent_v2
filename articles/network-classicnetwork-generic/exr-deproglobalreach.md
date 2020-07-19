<properties
    pageTitle="De-provisioning Issues - ExpressRoute Global Reach"
    description="De-provisioning Issues - ExpressRoute Global Reach"
    service="microsoft.network"
    resource="expressroutecircuits"
    authors="v-miegge"
    ms.author="v-miegge"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32627992"
    resourceTags=""
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="d22d5064-5d20-44d7-965a-a6a387691dd1"
	ownershipId="CloudNet_AzureExpressRoute"
/>

# De-provisioning Issues

## Connectivity to Azure Private, Azure Public, or Dynamics 365 Services

## **Recommended Steps**

You can delete your ExpressRoute circuit by selecting the delete icon. Please note the following information:

* You must unlink all virtual networks from the ExpressRoute circuit
* You or your service provider must delete all the BGP Peerings on the circuit
* If the ExpressRoute circuit service provider provisioning state is Provisioning or Provisioned, you must work with your service provider to de-provision the circuit on their side
* If the service provider has de-provisioned the circuit (the service provider provisioning state is set to **Not Provisioned**), you can delete the circuit. This stops billing for the circuit.

## **Recommended Documents**

* [De-provision and delete](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-portal-resource-manager#delete) an ExpressRoute circuit<br>
* [ExpressRoute Circuit Provisioning Workflow](https://docs.microsoft.com/azure/expressroute/expressroute-workflows)<br>
* [PowerShell](https://docs.microsoft.com/azure/expressroute/expressroute-howto-set-global-reach#disable-connectivity)<br>
* [CLI](https://docs.microsoft.com/azure/expressroute/expressroute-howto-set-global-reach-cli#disable-connectivity-between-your-on-premises-networks)
