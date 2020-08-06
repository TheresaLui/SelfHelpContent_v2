<properties
    pageTitle="ExpressRoute Peer IP Address Is Not A Public IP Address"
    description="ExpressRoute Peer IP Address Is Not A Public IP Address"
    infoBubbleText="ExpressRoute Peer IP Address Is Not A Public IP Address.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    ms.author="jaredr80"
    displayOrder=""
    articleId="ExRMicrosoftPeeringPeerIpIsNotAPublicIpAddressInsight"
    diagnosticScenario="ExRMicrosoftPeeringPeerIpIsNotAPublicIpAddressInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>

# ExpressRoute Peer IP Address is not a Public IP Address
<!--/issueDescription-->
Microsoft peering provides customers with the ability to access Microsoft public services (i.e. Azure Storage, Azure SQL, etc.) over a private connection, bypassing the Internet. The traffic for Microsoft peering does not enter a Virtual Routing Forwarding instance. Instead, routes advertised to Microsoft peering and the sub-interfaces are within the global routing table. Microsoft recommends public IPs for the peer IPs to ensure uniqueness and ownership.

* '**<!--$Message-->[Message]<!--/$Message-->**' <br>
* ServiceKey: '**<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**'  <br>
* MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' <br>
* VRF Name: '**<!--$VRF-->[VRF]<!--/$VRF-->**' <br>
<!--/issueDescription-->

## **Recommended Steps**

* Recommend that the customer change the peer IPs from private IPs to public IPs. The creation may fail if the IP addresses overlap with other customers on the same device.

## **Recommended Documenst**

* [ExpressRoute circuits and routing domains](https://docs.microsoft.com/azure/expressroute/expressroute-circuit-peerings#routing-domain-comparison)
