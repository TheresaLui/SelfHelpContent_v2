<properties 
    pageTitle="ExpressRoute Circuit reconciliation issue detected between NRP and Brooklyn"
    description="ExpressRoute Circuit reconciliation issue detected between NRP and Brooklyn"
    infoBubbleText="ExpressRoute Circuit reconciliation issue detected between NRP and Brooklyn.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    displayOrder=""
    articleId="ExpressRouteReconciliationIssueDetectedInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
# ExpressRoute Circuit reconciliation issue detected between NRP and Brooklyn
ExpressRoute circuit: '**<!--$CircuitName-->[CircuitName]<!--/$CircuitName-->**' NRP Service Provider Provisioning State is:  '**<!--$NrpServiceProviderProvisioningState-->[NrpServiceProviderProvisioningState]<!--/$NrpServiceProviderProvisioningState-->**' while Brooklyn shows Service Provider Provisioning State as:  '**<!--$BrooklynServiceProviderProvisioningState-->[BrooklynServiceProviderProvisioningState]<!--/$BrooklynServiceProviderProvisioningState-->**'.
 
## **Recommended steps**
An operation failed causing the state of the cricuit to become **Failed**. Traffic is not impacted in this scenario, but no further operations can be conducted on the circuit until it is no longer in a **Failed** state. 

1. From the portal, navigate to the circuit blade and click *Refresh*. This will make no changes to the circuit itself, but will move the state from **Failed**. 
2. From PowerShell, follow the instructions in the recommended document. 

## **Recommended document**
[Reset ExpressRoute peerings](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-howto-reset-peering) <br>