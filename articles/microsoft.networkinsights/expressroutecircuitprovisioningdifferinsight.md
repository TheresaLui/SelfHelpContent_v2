<properties
    pageTitle="NRP Service Provider Provisioning and Brooklyn Service Provider Provisioning differ"
    description="NRP Service Provider Provisioning and Brooklyn Service Provider Provisioning differ"
    infoBubbleText="NRP Service Provider Provisioning and Brooklyn Service Provider Provisioning differ.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    ms.author="jaredr80"
    displayOrder=""
    articleId="ExpressRouteCircuitProvisioningDifferInsight"
    diagnosticScenario="ExpressRouteCircuitProvisioningDifferInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>

# **NRP Service Provider Provisioning and Brooklyn Service Provider Provisioning Differ**
<!--/issueDescription-->
An operation failed, changing the state of the circuit **Failed**. Traffic is not impacted in this scenario, but no further operations can be conducted on the circuit until it is no longer in a **Failed** state.

ExpressRoute circuit: '**<!--$CircuitName-->[CircuitName]<!--/$CircuitName-->**'
NRP Service Provider Provisioning State is:  '**<!--$NrpServiceProviderProvisioningState-->[NrpServiceProviderProvisioningState]<!--/$NrpServiceProviderProvisioningState-->**' while Brooklyn shows Service Provider Provisioning State as:  '**<!--$BrooklynServiceProviderProvisioningState-->[BrooklynServiceProviderProvisioningState]<!--/$BrooklynServiceProviderProvisioningState-->**'.<br>
<!--/issueDescription-->

## **Recommended Steps**

1. From the [Azure portal](https://portal.azure.com), navigate to the circuit blade and click *Refresh*. This will make no changes to the circuit itself, but will move the state from **Failed**.
2. From PowerShell, follow the instructions in the document below

## **Recommended Document**

* [Reset ExpressRoute peerings](https://docs.microsoft.com/azure/expressroute/expressroute-howto-reset-peering)
