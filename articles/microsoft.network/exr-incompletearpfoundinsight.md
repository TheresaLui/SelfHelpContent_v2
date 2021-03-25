<properties
    pageTitle="Incomplete ARP(s) found"
    description="Incomplete ARP(s) found"
    infoBubbleText="Need more information about this issue? See details on the right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="TobyTu"
    ms.author="pareshmu, mariliu"
    displayOrder=""
    articleId="ExpressRouteIncompleteArpFoundInsight"
    selfHelpType="diagnostics"
    diagnosticScenario="ExpressRouteIncompleteArpFoundInsight"
    supportTopicIds="32627979"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
     ownershipId="CloudNet_AzureExpressRoute"
/>

# Incomplete ARP Entry Found
<!--issueDescription-->
We have identified that the Address Resolution Protocol (ARP) isn't established on your ExpressRoute circuit **<!--$CircuitName-->CircuitName<!--/$CircuitName-->** for peers **<!--$failedPeerList-->failedPeerList<!--/$failedPeerList-->**. To enable private connectivity to an Azure virtual network or public connectivity to an online Microsoft resource, ARP must be established first.
<!--/issueDescription-->

## **Recommended Steps**

Do one of the following: 

* If your ExpressRoute circuit is managed via an ExpressRoute partner, review the VLAN IDs set in any peering configured on the circuit. Also, make sure that your ExpressRoute partner has configured their end of the connection with the same VLAN IDs.

* If your ExpressRoute circuit is managed via ExpressRoute Direct, review the VLAN IDs set in any peering configured on the circuit. Also, make sure that your on-premises configuration matches the Azure configuration.
